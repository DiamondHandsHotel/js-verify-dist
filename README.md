<div id="top"></div>

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/DiamondHandsHotel/verify">
    <img src="images/logo.svg" alt="Verify logo" height="40" width="auto">
  </a>

  <h3 align="center">Verify - Javascript SDK</h3>

  <p align="center">
    Securely attach photos, videos, files and more to your NFTs.<br />Install in minutes, on any website, without changes to your smart contract.
    <br />
    <br />
    <a href="https://docs.dmnd.network/api-products/verify"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://diamondhandshotel.com/verify">View Demo</a>
    ·
    <a href="https://github.com/DiamondHandsHotel/verify/issues">Report Bug</a>
    ·
    <a href="https://github.com/DiamondHandsHotel/verify/issues">Request Feature</a>
  </p>
</div>


<!-- Demo/about -->
## About Verify

[![Demo of Verify in use][product-screenshot]](https://diamondhandshotel.com/verify)

Verify allows you to verify whether users own an NFT with one line of Javascript. It automatically handles connecting their wallet, signing a nonce and checking for ownership of NFTs under a specified contract.

You can also add unlockable content, which can only be accessed if they own a valid NFT. Unlockable content supports videos, images, digital downloads, and even allows you to build completely custom integrations with Webhooks.

It works seamlessly across Ethereum, Polygon and Solana, with more chains under active development. You can use the results returned directly on the frontend, and/or validate the signature on the backend to grant access to gated content.

<p align="right">(<a href="#top">back to top</a>)</p>


<!-- GETTING STARTED -->
## Getting Started

This is an example of how you may give instructions on setting up your project locally.
To get a local copy up and running follow these simple example steps.

### Install with NPM

1. Get a free API Key at [https://diamondhandshotel.com/verify](https://diamondhandshotel.com/verify)
2. Install the SDK

   ```sh
   npm install --save @diamondhh/verify
   ```
3. Initialize the SDK with your **public** API key

   ```js
   import VerifySdk from '@diamondhh/verify';
   // If you're only using a single chain you can also import a chain specific version
   // import VerifySdk from '@diamondhh/verify/ethereum'
   const verify = new VerifySdk('pk_YOUR_API_KEY');
   ```

### Install with <script>

1. Get a free API Key at [https://diamondhandshotel.com/verify](https://diamondhandshotel.com/verify)
2. Add the script tag before your closing body tag

   ```html
   <script src="https://unpkg.com/@diamondhh/verify/dist/verify.umd.js"></script>
   ```
3. Initialize the SDK with your **public** API key

   ```js
   var verify = new VerifySdk('pk_YOUR_API_KEY');
   ```

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Usage

Start a verification attempt by calling `verify.nft()` with a configuration object for the contract.
This returns a promise which will resolve on successful attempt (no errors), or reject if the user
closed the connection dialog or refused the wallet connection.

```js
await verify.nft({
  chain: 'ETH',
  contract: '0xbc4ca0eda7647a8ab7c2061c2e118a18a936f13d'
})
```

You can pass additional arguments to customise the connection window, link to marketplace listings
and request access to unlockable content.

_For more examples, please refer to the [Documentation](https://docs.dmnd.network/api-products/verify/browser-sdk)_

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- ROADMAP -->
## Roadmap

- [x] Ethereum ERC721 support
- [x] Polygon ERC721 support
- [x] Solana Metaplex support
- [ ] Ethereum ERC1155 support (WIP)
- [ ] Polygon ERC1155 support (WIP)
- [ ] Solana SPL Token support (WIP)

See the [open issues](https://github.com/DiamondHandsHotel/verify/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- CONTRIBUTING -->
## Contributing

This repository contains only prebuilt libraries for the Verify SDK, and the source is not
available at this time (though we have plans to release it!). As such, we're not accepting
code contributions.

If you have a suggestion that would make Verify better or a bug report (excluding security issues)
please open an issue.

If you've identified a security issue or bug please send us the details confidentially via our
website at https://diamondhandshotel.com/contact by selecting "Report a security issue" in the form.

Don't forget to give the project a star if you like it! Thanks again!

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the ISC License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Diamond Hands Hotel - [@DiamondHH](https://twitter.com/DiamondHH) - frontdesk@diamondhandshotel.com

Project Link: [https://github.com/DiamondHandsHotel/verify](https://github.com/DiamondHandsHotel/verify)

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* [ethers.js](https://github.com/ethers-io/ethers.js/)
* [Tailwind CSS](https://github.com/tailwindlabs/tailwindcss)

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
[product-screenshot]: images/demo.gif