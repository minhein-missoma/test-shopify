# Carpetright new storefront using Shopify
New webshop for Carpetright based on Shopify.

## BUILT WITH

- Shopify
- HTML [ *Liquid.js* ]
- CSS [ *TailwindCSS* ]
- Javascript
- React.js [ *Hooks, Refs* ]
- framer-motion
- eslint, Prettier
- react-scroll-parallax

#### BUILD & DEPLOYMENT

- vite
- Shopify CLI

## Requirements

### Shopify CLI

Follow the documentation [here](https://shopify.dev/docs/api/shopify-cli) to install the Shopify CLI (including Ruby)

## Repo Set Up

### Create `shopify.theme.toml` theme configuration:

- Copy `shopify.theme-example.toml` and rename to `shopify.theme.toml`
- Update the details in this new file with the correct details

#### Store
This is the Shopify URL associated with the store you are working on

#### Password
This is the password that provides you read and write access to your theme.

- In your Shopify admin panel, navigate to `apps` in the left hand sidebar
- Select `Theme Access`
- Create a new password if one doesn't exist or access the password associated with your name
- Copy this password and use for both environments in the newly created `shopify.theme.toml`

#### Theme
These IDs will be used to connect the Shopify themes to your code. They are referenced primarily in the `package.json` file

- To get the `live` ID, go into `Sales Channels` > `Online Store` > `Themes` and hit the three dots next to the live theme
- Select `Edit code` and at the end of the URL you will see a number ID that can be added to the `Live` environment set up
- Duplicate off the live theme to create a local theme and replicate the steps above but add the ID to the `dev` environment

#### Everything Else
Everything else can stay as default

### Install Dependancies

Ensure you have cd'd into the root file of the project (in the location where the `package.json` file is located) and run

`npm install`

This will install all the dependancies and provision the environment ready to be worked on.

## AVAILABLE SCRIPTS

In the project directory, you can run:

### `npm run dev`

Uploads the current theme as a development theme to the connected store, then prints theme editor and preview URLs to your terminal. While running, changes will push to the store in real time.

This command is set to run for the `dev` environment.

### `npm run build`

Compiles assets through Vite

### `npm run deploy`

Uploads your local theme files to the connected store, overwriting the remote version if specified.

This command is set to run for the `dev` environment.

### `npm run deploy:live`

Uploads your local theme files to the connected store, overwriting the remote version if specified.

This command is set to run for the `live` environment.

### `npm run download`

Download your remote theme files locally.

This command is set to run for the `dev` environment.
