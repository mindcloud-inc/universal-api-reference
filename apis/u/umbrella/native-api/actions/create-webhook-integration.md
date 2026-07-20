# Create Webhook Integration with Umbrella

Creates a new webhook integration in Umbrella.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.sse.cisco.com/admin/v2/integrations`
- **Base URL:** `https://api.umbrella.com`
- **Official documentation:** [Create Webhook Integration](https://developer.cisco.com/docs/cloud-security/create-integration/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | The integration name. |
| `type` | body | `string` | no | The integration type. |
| `webhookConfig.url` | body | `string` | no | The destination URL for webhook integrations. |
