# Create Webhook with GoCanvas

## Endpoint

- **Method:** `POST`
- **Path:** `/forms/:formId/webhooks`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Create Webhook](https://api.gocanvas.com/api/v3/docs#create-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `number` | yes | — |
| `event_type` | body | `list` | yes | Accepted values: `dispatch_create`, `submission_create`, `submission_custom_status_change`, `submission_edit`, `workflow_handoff_create`. |
| `format` | body | `list` | yes | XML is supported only for submission_create; all other event types require JSON. Accepted values: `json`, `xml`. |
| `push_url` | body | `string` | yes | — |
| `push_tag` | body | `string` | no | — |
