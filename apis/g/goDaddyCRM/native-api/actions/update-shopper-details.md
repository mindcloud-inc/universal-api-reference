# Update Shopper Details with GoDaddy CRM

Updates shopper details in your GoDaddy account.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/shoppers/:shopperId`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Update Shopper Details](https://developer.godaddy.com/doc/endpoint/shoppers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shopperId` | path | `string` | yes | Required shopper identifier to update |
| `marketId` | body | `string` | no | Optional updated market identifier |
