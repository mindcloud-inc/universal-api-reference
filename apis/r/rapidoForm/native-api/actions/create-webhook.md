# Create Webhook with RapidoForm

Creates a webhook for RapidoForm form submissions.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/webhook/save`
- **Base URL:** `https://www.rapidoform.com/be`
- **Official documentation:** [Create Webhook](https://www.rapidoform.com/developers/docs/webhooks)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `surveyId` | body | `string` | yes |
| `webhookUrl` | body | `string` | yes |
