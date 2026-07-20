# Get Invoice PDF Link with Envoice

Retrieves an invoice PDF URL from Envoice.

## Endpoint

- **Method:** `GET`
- **Path:** `invoice/pdf`
- **Base URL:** `https://www.envoice.in/api`
- **Official documentation:** [Get Invoice PDF Link](https://www.envoice.in/reference/api/docs/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `number` | yes | Invoice identifier. |
| `signedVersion` | query | `boolean` | no | Whether to return the signed PDF version. |
