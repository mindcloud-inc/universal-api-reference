# Add Webhook with Pipedrive

Creates a new webhook in Pipedrive.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/webhooks`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [Add Webhook](https://developers.pipedrive.com/docs/api/v1/Webhooks#addWebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscription_url` | body | `string` | yes | HTTPS callback URL to receive webhook payloads. |
| `event_action` | body | `string` | yes | Webhook event action: added, updated, deleted, *. |
| `event_object` | body | `string` | yes | Webhook event object: deal, person, organization, activity, note, product, lead, etc. |
| `version` | body | `string` | no | Webhook API version. |
