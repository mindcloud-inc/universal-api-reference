# Get Shopper Details with GoDaddy CRM

Retrieves shopper details from your GoDaddy account.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/shoppers/:shopperId`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Get Shopper Details](https://developer.godaddy.com/doc/endpoint/shoppers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shopperId` | path | `string` | yes | Required shopper identifier to retrieve |
| `includes` | query | `string<string>` | no | Optional additional shopper properties to include Send multiple values as a array. |
