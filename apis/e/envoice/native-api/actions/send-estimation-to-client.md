# Send Estimation to Client with Envoice

Sends an estimation to a client in Envoice.

## Endpoint

- **Method:** `POST`
- **Path:** `estimation/sendtoclient`
- **Base URL:** `https://www.envoice.in/api`
- **Official documentation:** [Send Estimation to Client](https://www.envoice.in/reference/api/docs/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `AttachPdf` | body | `boolean` | no | Whether to attach a PDF to the email. |
| `EstimationId` | body | `number` | yes | Estimation identifier to send. |
| `Message` | body | `string` | yes | Message to include in the estimation email. |
| `SendToSelf` | body | `boolean` | no | Whether to send a copy to the account owner. |
| `Subject` | body | `string` | no | Email subject. |
