# List Customer Invoices with PayWhirl

Retrieves a customer's invoices from PayWhirl.

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices/{customer_id}`
- **Base URL:** `https://api.paywhirl.com`
- **Official documentation:** [List Customer Invoices](https://api.paywhirl.com/#invoices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `all` | query | `number` | no | Set to 1 to return all invoices instead of only upcoming invoices. |
| `customer_id` | path | `number` | yes | The PayWhirl customer ID. |
| `subscription_id` | query | `number` | no | Filter invoices by subscription ID. |
| `tracking_number` | query | `string` | no | Filter invoices by tracking number. |
