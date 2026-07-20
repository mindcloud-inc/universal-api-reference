# Create Refund with Shippo - Legacy

Creates a refund for a Shippo shipping label.

## Endpoint

- **Method:** `POST`
- **Path:** `/refunds`
- **Base URL:** `https://api.goshippo.com`
- **Official documentation:** [Create Refund](https://docs.goshippo.com/shippoapi/public-api/refunds)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transaction` | body | `string` | yes | — |
| `apiKey` | path | `string` | no | Override the authentication API key here |
