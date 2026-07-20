# Delete Webhook with Typeform

## Endpoint

- **Method:** `DELETE`
- **Path:** `/forms/:formId/webhooks/:tag`
- **Base URL:** `https://api.typeform.com`
- **Official documentation:** [Delete Webhook](https://www.typeform.com/developers/webhooks/reference/delete-webhook/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | Typeform form identifier. |
| `tag` | path | `string` | yes | Webhook tag. |
