# Create Form Webhook with Jotform

Creates a webhook for a Jotform form.

## Endpoint

- **Method:** `POST`
- **Path:** `/form/:formId/webhooks`
- **Base URL:** `https://api.jotform.com`
- **Official documentation:** [Create Form Webhook](https://api.jotform.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | Form ID |
| `webhookURL` | query | `string` | yes | Destination URL to receive webhook events. |
