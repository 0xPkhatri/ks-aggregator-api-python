# KyberSwap Aggregator API Demo Python

This repository serves as a guide for developers looking to conduct swaps via the KyberSwap Aggregator APIs in a python environment. For simplicity, the examples are implemented in Python.

For more performant route querying and execution, please refer to the `[V1]` implementation which includes the following operations :

1. Query Swap Route (`getSwapRouteV1()`) - Fetches optimal swap routes based on input parameters
2. Encode Preferred Swap Route (`postSwapRouteV1()`) - Prepares the selected route for execution
3. Execute Swap Transaction On-Chain (`V1Swap()`) - Performs the actual swap transaction

To aid with readability, each operation has its own `.py` file which has been categorized under the `/src/operations/` folder. Users can run specific operations by commenting or uncommenting the relevant function in `index.py`.

## Getting Started

Prerequisites:

- Python 3.7 or higher
- pip package manager

To run the examples:

1. Clone this repository
2. Install dependencies: `pip install -r requirements.txt`
3. Set up environment variables in `.env` file:

   ```
   PRIVATE_KEY=your_private_key          # Your wallet's private key
   RPC_URL=your_rpc_url                  # URL of your preferred EVM RPC node
   ```

4. Set up the [web3.py Account](https://web3py.readthedocs.io/en/stable/web3.eth.account.html#accounts) under `/src/libs/account.py`
5. Run the example: `python src/index.py`

## API Specifications

Full API specifications, dev guide, and related sequence diagrams are available on [KyberSwap Docs](https://docs.kyberswap.com/kyberswap-solutions/kyberswap-aggregator/aggregator-api-specification/evm-swaps):

- [Executing A Swap With The Aggregator API](https://docs.kyberswap.com/kyberswap-solutions/kyberswap-aggregator/developer-guides/execute-a-swap-with-the-aggregator-api)
- [Upgrading To APIv1](https://docs.kyberswap.com/kyberswap-solutions/kyberswap-aggregator/developer-guides/upgrading-to-apiv1)

## Additional Notes

This project is inspired by the [ks-aggregator-api-demo](https://github.com/KyberNetwork/ks-aggregator-api-demo/tree/master) and adapts its functionality to a Python environment.

Note that the code samples in this repository are not production-ready and are meant as references to get you started on integrating KyberSwap Aggregator functionality into your dApp.
