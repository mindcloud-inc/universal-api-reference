# Subscribe Webhook with FillFaster

Subscribes a webhook URL to a FillFaster form.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/form/:formId/webhook/subscribe`
- **Base URL:** `https://api.fillfaster.com`
- **Official documentation:** [Subscribe Webhook](https://documenter.getpostman.com/view/18912453/2s8ZDVZ3UJ#115ff600-bfc7-4954-ac9e-b79402abba71)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events[]` | body | `array<string>` | no | Webhook event names to subscribe. |
| `formId` | path | `string` | yes | FillFaster form identifier. |
| `url` | body | `string` | yes | Webhook destination URL. |
