# Retrieve Single Webhook with Typeform

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:formId/webhooks/:tag`
- **Base URL:** `https://api.typeform.com`
- **Official documentation:** [Retrieve Single Webhook](https://www.typeform.com/developers/webhooks/reference/retrieve-single-webhook/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | Typeform form identifier. |
| `tag` | path | `string` | yes | Webhook tag. |
