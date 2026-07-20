# Update Integration with Umbrella

Updates an existing integration in Umbrella.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://api.sse.cisco.com/admin/v2/integrations/:intId`
- **Base URL:** `https://api.umbrella.com`
- **Official documentation:** [Update Integration](https://developer.cisco.com/docs/cloud-security/update-integration/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `intId` | path | `string` | no | The integration ID. |
| `name` | body | `string` | no | The updated integration name. |
| `webhookConfig.url` | body | `string` | no | The updated webhook destination URL. |
