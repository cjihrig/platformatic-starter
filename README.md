# Welcome to platformatic-starter 👋

![Version](https://img.shields.io/badge/version-0.1.0-blue.svg?cacheSeconds=2592000)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](#)
[![Twitter: jellydn](https://img.shields.io/twitter/follow/jellydn.svg?style=social)](https://twitter.com/jellydn)

> platformatic quick start demo app

## Install

```sh
yarn install
```

## Usage

```sh
yarn dev
```

## Deployment

This template comes with two GitHub Actions that handle automatically deploying your app to production and staging environments.

Prior to your first deployment, you'll need to do a few things:

- [Install Fly](https://fly.io/docs/getting-started/installing-flyctl/)

- Sign up and log in to Fly

  ```sh
  fly auth signup
  ```

- Create a new app on Fly:

  ```sh
  fly apps create platformatic-starter
  ```

- Create a new [GitHub Repository](https://repo.new)

- Add a `FLY_API_TOKEN` to your GitHub repo. To do this, go to your user settings on Fly and create a new [token](https://web.fly.io/user/personal_access_tokens/new), then add it to [your repo secrets](https://docs.github.com/en/actions/security-guides/encrypted-secrets) with the name `FLY_API_TOKEN`.

- Create a persistent volume for the sqlite database for both your app. Run the following:

  ```sh
  fly volumes create data --size 1 --app platformatic-starter
  ```

Now that every is set up you can commit and push your changes to your repo. Every commit to your `main` branch will trigger a deployment to your production environment.

## GitHub Actions

We use GitHub Actions for continuous integration and deployment. Anything that gets into the `main` branch will be deployed to production after running tests/build/etc.

## Useful references

- [Quick Start Guide](https://oss.platformatic.dev/docs/getting-started/quick-start-guide)
- [Movie Quotes App Tutorial](https://oss.platformatic.dev/docs/getting-started/movie-quotes-app-tutorial)
- [Add Custom Functionality](https://oss.platformatic.dev/docs/guides/add-custom-functionality/introduction)
- [Deploy to Fly.io](https://oss.platformatic.dev/docs/next/guides/deployment/deploy-to-fly-io-with-sqlite)

## Author

👤 **Dung Huynh**

- Website: https://productsway.com/
- Twitter: [@jellydn](https://twitter.com/jellydn)
- Github: [@jellydn](https://github.com/jellydn)

## Show your support

Give a ⭐️ if this project helped you!

---

_This README was generated with ❤️ by [readme-md-generator](https://github.com/kefranabg/readme-md-generator)_
