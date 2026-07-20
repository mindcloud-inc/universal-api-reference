# Create Custom Object with LoginRadius

Creates a new custom object in LoginRadius.

## Endpoint

- **Method:** `POST`
- **Path:** `/identity/v2/auth/customobject`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [Create Custom Object](https://www.loginradius.com/docs/api/openapi/create-custom-object-by-token/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `access_token` | query | `string` | yes | Access token for the logged-in user. |
| `objectname` | query | `string` | yes | Custom object collection name. |
| `customobjectid` | query | `string` | yes | Custom object record id. |
| `label` | body | `string` | yes | Label stored in the custom object body. |
| `active` | body | `boolean` | no | Whether the custom object is active. |
