# Subscribe Webhook with Rowform

Creates a webhook subscription in Rowform.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/zapier/hooks`
- **Base URL:** `https://app.rowform.io`
- **Official documentation:** [Subscribe Webhook](https://help.rowform.io/api-reference#subscribe-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hookUrl` | body | `string` | yes | The HTTPS URL that Rowform should POST webhook deliveries to. |
| `event` | body | `string` | yes | The Rowform event type to subscribe to. The current public docs show form.response.created. |
| `formId` | body | `string` | yes | The Rowform form id that should emit webhook events. |
