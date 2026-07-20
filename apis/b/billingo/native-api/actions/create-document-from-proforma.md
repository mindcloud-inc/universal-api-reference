# Create Document From Proforma with Billingo

Creates a document from a proforma in Billingo.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/:id/create-from-proforma`
- **Base URL:** `https://api.billingo.hu/v3`
- **Official documentation:** [Create Document From Proforma](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Billingo proforma document ID. |
| `fulfillment_date` | body | `date` | no | Optional fulfillment date for the new document. |
| `due_date` | body | `date` | no | Optional due date for the new document. |
| `comment` | body | `string` | no | Optional comment for the new document. |
