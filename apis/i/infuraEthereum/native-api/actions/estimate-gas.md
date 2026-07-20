# Estimate Gas with Infura Ethereum

Retrieves a gas estimate from Infura Ethereum.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/:apiKey`
- **Base URL:** `https://mainnet.infura.io`
- **Official documentation:** [Estimate Gas](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_estimategas/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params[0][data]` | body | `string` | yes | ABI-encoded function selector and arguments used for the estimate. |
| `params[0][to]` | body | `string` | yes | The target contract or recipient address for the gas estimate. |
| `params[1]` | body | `string` | yes | The block number or canonical tag to estimate against. |
