# Delete Custom Object by ID with LoginRadius

Deletes an existing custom object from LoginRadius by ID.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/identity/v2/auth/customobject/:objectrecordid`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [Delete Custom Object by ID](https://www.loginradius.com/docs/api/openapi/delete-custom-object-by-token-and-record-id/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `objectrecordid` | path | `string` | yes | Record identifier of the custom object entry to delete. |
| `access_token` | query | `string` | yes | Access Token of the user owning the custom object record. |
| `objectname` | query | `string` | yes | Custom object name configured in LoginRadius. |
| `customobjectid` | query | `string` | no | Custom object schema identifier when required by the tenant. |
| `prevent_webhook` | query | `boolean` | no | Whether to suppress LoginRadius webhook processing for the delete operation. |
