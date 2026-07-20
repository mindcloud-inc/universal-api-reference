# Delete Integration with Umbrella

Deletes an existing integration from Umbrella.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://api.sse.cisco.com/admin/v2/integrations/:intId`
- **Base URL:** `https://api.umbrella.com`
- **Official documentation:** [Delete Integration](https://developer.cisco.com/docs/cloud-security/delete-integration/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `intId` | path | `string` | no | The integration ID. |
