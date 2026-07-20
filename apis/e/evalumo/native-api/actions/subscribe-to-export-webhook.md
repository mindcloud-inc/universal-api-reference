# Subscribe To Export Webhook with Evalumo

Creates an export webhook subscription in Evalumo.

## Endpoint

- **Method:** `POST`
- **Path:** `/hook`
- **Base URL:** `https://api.evalumo.com`
- **Official documentation:** [Subscribe To Export Webhook](https://evalumo.apidocumentation.com/reference#tag/webhooks/POST/hook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hookUrl` | body | `string` | yes | Destination URL that will receive export webhook POST requests. |
| `hookId` | body | `string` | yes | Unique identifier for this webhook registration. |
| `hookName` | body | `string` | yes | Human-readable webhook subscription name. |
| `zapIcon` | body | `string` | no | Optional icon slug shown in Evalumo's webhook registration. |
| `triggerKey` | body | `string` | yes | Webhook event key, for example new_exported_project. |
| `lineItemsToExpand` | body | `string` | no | Optional comma-separated line item sections to include in webhook payloads. |
