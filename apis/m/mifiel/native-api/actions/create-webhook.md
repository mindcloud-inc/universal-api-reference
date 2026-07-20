# Create Webhook with Mifiel

Creates a new webhook endpoint in Mifiel.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/webhooks`
- **Base URL:** `https://app.mifiel.com`
- **Official documentation:** [Create Webhook](https://docs.mifiel.com/en/#tag/Webhooks/operation/CreateWebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Webhook URL endpoint. |
| `callback_type` | body | `string` | yes | Type of event that triggers this webhook: document_closed, signer_completed, signer_rejected, or document_deleted. |
