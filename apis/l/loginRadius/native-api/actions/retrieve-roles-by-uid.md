# Retrieve Roles by UID with LoginRadius

Retrieves assigned roles from LoginRadius by UID.

## Endpoint

- **Method:** `GET`
- **Path:** `/identity/v2/manage/account/:uid/role`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [Retrieve Roles by UID](https://www.loginradius.com/docs/api/openapi/get-roles-by-uid/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | UID of the user. |
