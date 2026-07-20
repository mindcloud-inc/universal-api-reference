# Check Permission with DigiCert

Checks whether the authenticated user has a DigiCert permission.

## Endpoint

- **Method:** `GET`
- **Path:** `/authorization/:permission`
- **Base URL:** `https://www.digicert.com/services/v2`
- **Official documentation:** [Check Permission](https://dev.digicert.com/certcentral-apis/services-api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `permission` | path | `string` | yes | The DigiCert permission name to check. |
