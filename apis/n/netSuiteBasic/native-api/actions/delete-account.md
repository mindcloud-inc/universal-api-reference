# Delete Account with NetSuite - Basic

Deletes an existing account from NetSuite.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/record/v1/account/:id`
- **Base URL:** `https://{accountDomain}.suitetalk.api.netsuite.com/services/rest`
- **Official documentation:** [Delete Account](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Internal NetSuite record ID. |
