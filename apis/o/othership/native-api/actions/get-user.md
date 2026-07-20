# Get User with Othership

Retrieves a specific user from Othership.

## Endpoint

- **Method:** `GET`
- **Path:** `/Users/:id`
- **Base URL:** `https://hwms-api.othership.com/api/v1/azure/scim`
- **Official documentation:** [Get User](https://www.ietf.org/rfc/rfc7644)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The SCIM user identifier. |
| `attributes` | query | `string` | no | Comma-separated SCIM attributes to include in the response. |
| `excludedAttributes` | query | `string` | no | Comma-separated SCIM attributes to omit from the response. |
