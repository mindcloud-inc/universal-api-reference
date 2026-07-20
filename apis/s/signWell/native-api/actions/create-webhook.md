# Create Webhook with SignWell

Creates a new webhook subscription in SignWell.

## Endpoint

- **Method:** `POST`
- **Path:** `/hooks/`
- **Base URL:** `https://www.signwell.com/api/v1`
- **Official documentation:** [Create Webhook](https://developers.signwell.com/reference/post_api-v1-hooks-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `callback_url` | body | `string` | yes | URL that SignWell will post document events to. |
| `api_application_id` | body | `string` | no | Unique identifier for the API Application. |
