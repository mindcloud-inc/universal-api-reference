# List Webhooks with Moaform

Retrieves webhooks for a form in Moaform.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:formId/webhooks`
- **Base URL:** `https://api.moaform.com/v1`
- **Official documentation:** [List Webhooks](https://help.moaform.com/hc/en-us/articles/28408524240537-Fetching-Webhook-Information)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | path | `string` | yes | Unique ID of the form. |
