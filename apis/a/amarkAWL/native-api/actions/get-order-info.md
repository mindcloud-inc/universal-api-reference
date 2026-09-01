# Get Order Info with Amark

## Endpoint

- **Method:** `POST`
- **Path:** `/Order/Info`
- **Base URL:** `{environment}`
- **Official documentation:** [Get Order Info](https://vaultlinkapi-sandbox.gold.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderNumber` | body | `string` | yes | Required. Enter the Order Number that matches the Order ID. |
| `orderId` | body | `number` | yes | Required. Enter the numeric Order ID that matches the Order Number. |
