# Create Smart Contract Webhook with Overledger

## Endpoint

- **Method:** `POST`
- **Path:** `/api/webhooks/smart-contract-events`
- **Base URL:** `https://api.overledger.dev`
- **Official documentation:** [Create Smart Contract Webhook](https://docs.overledger.dev/docs/smart-contract)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `API-Version` | `3.0.0` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location` | body | `object` | yes | Overledger location object with technology and network. |
| `callbackUrl` | body | `string` | yes | Public callback URL that Overledger will send webhook events to. |
| `smartContractId` | body | `string` | yes | Smart contract identifier/address to monitor. |
