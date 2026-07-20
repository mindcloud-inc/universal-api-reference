# Send Template Messages with Wati

Sends template messages to multiple contacts in Wati.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/sendTemplateMessages`
- **Base URL:** `{apiEndpointUrl}`
- **Official documentation:** [Send Template Messages](https://docs.wati.io/reference/post_api-v1-sendtemplatemessages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_name` | body | `string` | yes | Approved Wati template name. |
| `broadcast_name` | body | `string` | yes | Name for the broadcast record. |
| `receivers[]` | body | `array<object>` | yes | Recipients and custom parameters for the broadcast. |
