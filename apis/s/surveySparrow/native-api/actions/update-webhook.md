# Update Webhook with SurveySparrow

Updates an existing webhook in SurveySparrow.

## Endpoint

- **Method:** `PUT`
- **Path:** `/webhooks/{{id}}`
- **Base URL:** `https://api.surveysparrow.com/v3`
- **Official documentation:** [Update Webhook](https://developers.surveysparrow.com/rest-apis/put-v-3-webhooks-id/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Webhook ID |
| `name` | body | `string` | no | Webhook name |
| `description` | body | `string` | no | Webhook description |
| `url` | body | `string` | no | Webhook URL |
| `http_method` | body | `list` | no | HTTP method |
| `headers[]` | body | `array<object>` | no | Header array |
| `payload` | body | `object` | no | Payload object |
| `include_partial_submission` | body | `boolean` | no | Include partial submissions |
