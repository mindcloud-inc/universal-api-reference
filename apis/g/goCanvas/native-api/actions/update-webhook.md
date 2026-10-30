# Update Webhook with GoCanvas

## Endpoint

- **Method:** `PATCH`
- **Path:** `/forms/:formId/webhooks/:webhookId`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Update Webhook](https://api.gocanvas.com/api/v3/docs#update-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `number` | yes | — |
| `webhookId` | path | `number` | yes | — |
| `event_type` | body | `list` | no | Accepted values: `dispatch_create`, `submission_create`, `submission_custom_status_change`, `submission_edit`, `workflow_handoff_create`. |
| `format` | body | `list` | no | XML is supported only for submission_create; all other event types require JSON. Accepted values: `json`, `xml`. |
| `push_url` | body | `string` | no | — |
| `push_tag` | body | `string` | no | — |
