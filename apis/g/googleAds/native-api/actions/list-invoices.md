# List Invoices with Google Ads

Retrieves invoices from your Google Ads account.

## Endpoint

- **Method:** `GET`
- **Path:** `v22/customers/:customerId/invoices`
- **Base URL:** `https://googleads.googleapis.com/`
- **Official documentation:** [List Invoices](https://developers.google.com/google-ads/api/reference/rpc/v22/InvoiceService/ListInvoices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | Customer ID that owns the Google Ads resources (without dashes). |
| `billingSetup` | query | `string` | yes | Billing setup resource name, for example customers/1234567890/billingSetups/1111111111. |
| `issueYear` | query | `number` | yes | Invoice issue year (YYYY). |
| `issueMonth` | query | `string` | yes | Invoice issue month enum value, for example JANUARY or MARCH. |
