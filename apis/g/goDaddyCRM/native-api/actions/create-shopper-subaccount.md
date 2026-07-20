# Create Shopper Subaccount with GoDaddy CRM

Creates a shopper subaccount in GoDaddy.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/shoppers/subaccount`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Create Shopper Subaccount](https://developer.godaddy.com/doc/endpoint/shoppers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nameFirst` | body | `string` | yes | Required shopper first name |
| `nameLast` | body | `string` | yes | Required shopper last name |
| `email` | body | `string` | yes | Required subaccount email address |
| `password` | body | `string` | yes | Required password for the new subaccount |
| `marketId` | body | `string` | no | Optional BCP-47 market identifier. Defaults to en-US. |
| `externalId` | body | `number` | no | Optional external numeric identifier for the subaccount |
