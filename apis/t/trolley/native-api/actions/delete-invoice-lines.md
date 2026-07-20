# Delete Invoice Lines with Trolley

Deletes existing invoice lines from Trolley.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/invoices/delete-lines`
- **Base URL:** `https://api.trolley.com`
- **Official documentation:** [Delete Invoice Lines](https://developers.trolley.com/api/#delete-an-invoice-line)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoiceId` | body | `string` | no | Invoice ID |
