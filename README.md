# Welcome to Great Bull Society Collection 💎

![](https://github.com/fauzi2nd/GreatBullSociety/blob/main/logo-blob.png)

All the code in these repos was created and explained by HashLips on the main YouTube channel.

To find out more please visit:

[💬 Telegram](https://t.me/GreatBullSociety)

[🐦 Twitter](https://twitter.com/GreatBullSoc)

[ℹ️ Website](https://GreatBullSociety.app/)

[o Opensea](https://opensea.io/collection/great-bull-society)

# Great Bull Society minting dapp 🔥

This repo provides a nice and easy way for linking an existing NFT smart contract to this minting dapp. There are two ways of using this repo, you can go the simple route or the more complex one.

The simple route is so simple, all you need to do is download the build folder on the release page and change the configuration to fit your needs. (Follow the video for a walk through).

The more complex route allows you to add additional functionality if you are comfortable with coding in react.js. (Follow the below instructions for a walk through).

## Installation 🛠️

If you are cloning the project then run this first, otherwise you can download the source code on the release page and skip this step.

```sh
git clone https://github.com/fauzi2nd/GreatBullSociety.git
```

Make sure you have node.js installed so you can use npm, then run:

```sh
npm install
```

## Usage ℹ️

In order to make use of this dapp, all you need to do is change the configurations to point to your smart contract as well as update the images and theme file.

For the most part all the changes will be in the `public` folder.

To link up your existing smart contract, go to the `public/config/config.json` file and update the following fields to fit your smart contract, network and marketplace details. The cost field should be in wei.

Note: this dapp is designed to work with the intended NFT smart contract, that only takes one parameter in the mint function "mintAmount". But you can change that in the App.js file if you need to use a smart contract that takes 2 params.

```json
{
  "CONTRACT_ADDRESS": "0x2E928E0c70396a6C2e660eB7Cb3a11003bFBF8Cf",
  "SCAN_LINK": "https://polygonscan.com/token/0x2E928E0c70396a6C2e660eB7Cb3a11003bFBF8Cf",
  "NETWORK": {
    "NAME": "Polygon",
    "SYMBOL": "Matic",
    "ID": 137
  },
  "NFT_NAME": "Great Bull Society",
  "SYMBOL": "BULL",
  "MAX_SUPPLY": 10000,
  "WEI_COST": 2000000000000000000,
  "DISPLAY_COST": 2,
  "GAS_LIMIT": 285000,
  "MARKETPLACE": "Opeansea",
  "MARKETPLACE_LINK": "https://opensea.io/collection/great-bull-society",
  "SHOW_BACKGROUND": true
}
```

Make sure you copy the contract ABI from remix and paste it in the `public/config/abi.json` file.
(follow the youtube video if you struggle with this part).

Now you will need to create and change 2 images and a gif in the `public/config/images` folder, `bg.png`, `example.gif` and `logo.png`.

Next change the theme colors to your liking in the `public/config/theme.css` file.

```css
:root {
  --primary: #ebc908;
  --primary-text: #1a1a1a;
  --secondary: #ff1dec;
  --secondary-text: #ffffff;
  --accent: #ffffff;
  --accent-text: #000000;
}
```

Now you will need to create and change the `public/favicon.ico`, `public/logo192.png`, and
`public/logo512.png` to your brand images.

Remember to update the title and description the `public/index.html` file

```html
<title>Great Bull Society</title>
<meta name="description" content="Great Bull Society" />
```

Also remember to update the short_name and name fields in the `public/manifest.json` file

```json
{
  "short_name": "BULL",
  "name": "Great Bull Society"
}
```

After all the changes you can run.

```sh
npm run start
```

Or create the build if you are ready to deploy.

```sh
npm run build
```

Now you can host the contents of the build folder on a server.

That's it! you're done.
