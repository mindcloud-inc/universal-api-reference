# Create Outgoing Webhook with Uspacy

Creates a new outgoing webhook in Uspacy.

## Endpoint

- **Method:** `POST`
- **Path:** `/company/v1/webhooks`
- **Base URL:** `https://{site}`
- **Official documentation:** [Create Outgoing Webhook](https://uspacy.readme.io/reference/post_company-v1-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The outgoing webhook target URL. |
| `events[].service` | body | `string` | yes | Webhook event service. |
| `events[].type` | body | `string` | yes | Webhook event type. |
| `events[].table_name` | body | `string` | no | Optional CRM table name for entity CRM events. |
| `events[].actions[]` | body | `array<string>` | yes | Webhook event actions. |
