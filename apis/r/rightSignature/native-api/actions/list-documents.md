# List Documents with RightSignature

Retrieves available documents from your RightSignature account.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents`
- **Base URL:** `https://api.rightsignature.com/public/v2`
- **Official documentation:** [List Documents](https://api.rightsignature.com/documentation/resources/v2/documents/index.en.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | A search token. |
| `template_id` | query | `string` | no | Documents from a specific template |
| `state` | query | `string` | no | The document state filter. Must be one of valid document states or comma seperated list of states. Valid document states are: draft, pending, executed, voided, expired, declined, editing |
