# List Subaccounts with Seven

Retrieves subaccounts from Seven.

## Endpoint

- **Method:** `GET`
- **Path:** `/subaccounts?action=read`
- **Base URL:** `https://gateway.seven.io/api`
- **Official documentation:** [List Subaccounts](https://docs.seven.io/en/rest-api/endpoints/subaccounts#list-subaccounts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `number` | no | The ID of a subaccount. This will give you only the data for a specific subaccount. |
