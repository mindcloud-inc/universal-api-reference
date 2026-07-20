# Unsubscribe Webhook with FillFaster

Removes a webhook URL from a FillFaster form.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/form/:formId/webhook/unsubscribe`
- **Base URL:** `https://api.fillfaster.com`
- **Official documentation:** [Unsubscribe Webhook](https://documenter.getpostman.com/view/18912453/2s8ZDVZ3UJ#0ec7d0f3-0bc0-4723-9816-00153a6a9e85)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | FillFaster form identifier. |
| `url` | body | `string` | yes | Webhook destination URL to remove. |
