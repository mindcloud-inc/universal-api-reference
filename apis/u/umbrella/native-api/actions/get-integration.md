# Get Integration with Umbrella

Retrieves integration details from your Umbrella organization.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.sse.cisco.com/admin/v2/integrations/:intId`
- **Base URL:** `https://api.umbrella.com`
- **Official documentation:** [Get Integration](https://developer.cisco.com/docs/cloud-security/get-integration/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `intId` | path | `string` | no | The integration ID. |
