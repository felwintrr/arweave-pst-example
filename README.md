## Creating and Deploying a PST To Arweave

This is the companion repo of the source code used in OnlyArweave's PST creation article/video. 

**The `TEST_PST` token created in this tutorial is purely for
demonstration purposes, holds no monetary value, and should not be considered an asset of any kind.**

If you would like to clone this repo and test out the code for yourself, follow the configuration steps below. **Make sure to abide by the rules and regulations of your country
before deploying, creating or selling PSTs.**

### Configuration

- Run `npm install`
- Edit the [token configuration file](token-pst.json) and set the ticker/preferred symbol, the owner address, and amount of tokens you want to create (which will be distributed to the addresses entered in balances).

### Deployment 

- Add your Arweave keyfile to the directory (make sure you do **not** share this publicly or upload it to GitHub!)
- Run `smartweave create ff8wOKWGIS6xKlhA8U6t70ydZOozixF5jQMp4yjoTc8 token-pst.json --key-file keyfile.json ` where `keyfile.json` is the name of your keyfile.

This command will leverage an already deployed SmartWeave contract to create and launch the PST.

### Testing the Front End

- Open the code for the [web page](pages/index.js) and replace `pstContractId` with your own contract ID.
- Run `npm run dev` and wait for the server to start
- Click the `Send Fee!` button and wait for an ArConnect popup. Once the transaction is signed, it will be posted and the chosen weighted PST holder will receive 0.1 AR.
