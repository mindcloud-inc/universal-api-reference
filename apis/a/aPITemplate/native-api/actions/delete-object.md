# Delete Object with API Template

Deletes an existing generated object from API Template.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/delete-object`
- **Base URL:** `https://rest.apitemplate.io`
- **Official documentation:** [Delete Object](https://apitemplate.io/apiv2/#tag/API-Integration/operation/delete-object)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transaction_ref` | query | `string` | yes | Transaction reference of the object to delete. |
