# Create Transfer with Dwolla

Creates a new transfer in Dwolla.

## Endpoint

- **Method:** `POST`
- **Path:** `/transfers`
- **Base URL:** `https://api-sandbox.dwolla.com`
- **Official documentation:** [Create Transfer](https://developers.dwolla.com/docs/api-reference/transfers/initiate-a-transfer)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `_links.source.href` | body | `string` | yes | Source funding source URL |
| `_links.destination.href` | body | `string` | yes | Destination funding source URL |
| `amount.currency` | body | `string` | yes | Transfer currency |
| `amount.value` | body | `string` | yes | Transfer amount value |
