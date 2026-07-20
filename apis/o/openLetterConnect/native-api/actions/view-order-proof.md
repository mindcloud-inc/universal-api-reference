# View Order Proof with Open Letter Connect

Retrieves an order proof from Open Letter Connect.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/view-proof`
- **Base URL:** `https://api.openletterconnect.com/api/v1`
- **Official documentation:** [View Order Proof](https://api-docs.openletterconnect.com/orders/view-proof/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | body | `string` | no | The existing order ID to generate a proof for. |
| `templateId` | body | `number` | no | The template ID to render a proof for. |
| `contactId` | body | `number` | no | The contact ID to render in the proof. |
| `returnContactId` | body | `number` | no | The return contact ID to use for the proof. |
