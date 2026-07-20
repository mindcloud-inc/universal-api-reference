# Create Webhook with Weavely

Creates a webhook for a Weavely form.

## Endpoint

- **Method:** `POST`
- **Path:** `/forms/:formId/webhooks`
- **Base URL:** `https://api.weavely.ai/v1`
- **Official documentation:** [Create Webhook](https://help.weavely.ai/developers/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The ID of the form to attach the webhook to. |
| `url` | body | `string` | yes | The destination URL that will receive POST payloads when a form is submitted. |
