# Retrieve Custom Objects with LoginRadius

Retrieves custom object records from LoginRadius.

## Endpoint

- **Method:** `GET`
- **Path:** `/identity/v2/auth/customobject`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [Retrieve Custom Objects](https://www.loginradius.com/docs/api/openapi/get-custom-object-by-token/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `access_token` | query | `string` | yes | Access token of the user. |
| `customobjectid` | query | `string` | no | Specific custom object record ID. |
| `objectname` | query | `string` | yes | Configured custom object name. |
