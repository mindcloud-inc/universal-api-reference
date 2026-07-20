# Create Webhook Endpoint with Ablefy

Creates a new webhook endpoint in Ablefy.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/webhook_endpoints`
- **Base URL:** `https://api.myablefy.com`
- **Official documentation:** [Create Webhook Endpoint](https://api.myablefy.com/api/swagger_doc/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
| `url` | body | `string` | yes | — |
| `event_form` | body | `list<string>` | no | Accepted values: `all_events`, `selected_events`. |
| `event_ids[]` | body | `array<string>` | no | — |
| `request_format` | body | `list<string>` | no | Accepted values: `json`, `x_www_form_urlencoded`. |
