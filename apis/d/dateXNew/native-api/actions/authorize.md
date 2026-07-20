# Authorize with DateX

## Endpoint

- **Method:** `POST`
- **Path:** `https://login.microsoftonline.com/6498fd5a-7169-49a0-a87e-2107759e83e2/oauth2/v2.0/token`
- **Base URL:** `https://{environment}.wavelength.host/api/`
- **Official documentation:** [Authorize](https://sku-mindcloud-api.wavelength.host/documentation/custom.js)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | body | `string` | no | Azure client ID. |
| `client_secret` | body | `string` | no | Azure client secret. |
| `grant_type` | body | `string` | no | OAuth grant type. |
| `scope` | body | `string` | no | Azure token scope. |
| `url` | path | `string` | no | Token URL. |
