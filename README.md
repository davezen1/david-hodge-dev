# DavidHodge.dev Blog Site

![Build and Deploy](https://github.com/davezen1/david-hodge-dev/workflows/Build%20and%20Deploy/badge.svg)

- Uses Hugo and Firebase to host blog
- Uses GitHub Actions to automate build and deploy


```
name: Build and Deploy
on:
  push:
    branches:
      - master

jobs:
  build:
    name: Build
    runs-on: ubuntu-latest
    steps:
      - name: Checkout Repo
        uses: actions/checkout@master
      
      - name: Setup Hugo
        uses: peaceiris/actions-hugo@v2
        with:
          hugo-version: '0.70.0'
          # extended: true

      - name: Build
        run: hugo --minify
      
      - name: Archive Production Artifact
        uses: actions/upload-artifact@master
        with:
          name: public
          path: public
  deploy:
    name: Deploy
    needs: build
    runs-on: ubuntu-latest
    steps:
      - name: Checkout Repo
        uses: actions/checkout@master

      - name: Download Artifact
        uses: actions/download-artifact@master
        with:
          name: public

      - name: check contents of runner directory
        run: ls -R /home/runner/work/david-hodge-dev/david-hodge-dev

      - name: Deploy to Firebase
        uses: w9jds/firebase-action@master
        with:
          args: deploy --only hosting
        env:
          FIREBASE_TOKEN: ${{ secrets.FIREBASE_TOKEN }}

```
