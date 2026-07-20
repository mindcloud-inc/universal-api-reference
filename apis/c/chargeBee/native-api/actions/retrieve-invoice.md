# Retrieve Invoice with ChargeBee

Retrieves an invoice from ChargeBee.

## Endpoint

- **Method:** `GET`
- **Path:** `invoices/:invoice_id`
- **Base URL:** `https://{baseUrl}.chargebee.com/api/v2/`
- **Official documentation:** [Retrieve Invoice](https://apidocs.chargebee.com/docs/api/invoices/retrieve-an-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice_id` | path | `string` | yes | The Chargebee invoice identifier. |
