# Create Webhook with SurveySparrow

Creates a new webhook in SurveySparrow.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.surveysparrow.com/v3`
- **Official documentation:** [Create Webhook](https://developers.surveysparrow.com/rest-apis/post-v-3-webhooks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Webhook name |
| `description` | body | `string` | no | Webhook description |
| `url` | body | `string` | yes | Webhook URL |
| `event_type` | body | `string` | no | Webhook event type |
| `object_type` | body | `string` | no | Object type |
| `survey_id` | body | `number` | yes | Survey ID |
| `http_method` | body | `list` | yes | HTTP method |
| `headers[]` | body | `array<object>` | no | Header array |
| `type` | body | `string` | no | Webhook type |
| `payload` | body | `object` | no | Payload object |
| `include_partial_submission` | body | `boolean` | no | Include partial submissions |
