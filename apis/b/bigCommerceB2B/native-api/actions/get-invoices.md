# Get invoices with BigCommerce (B2B)

## Endpoint

- **Method:** `GET`
- **Path:** `ip/invoices`
- **Base URL:** `https://api-b2b.bigcommerce.com/api/v3/io/`
- **Official documentation:** [Get invoices](https://developer.bigcommerce.com/b2b-edition/apis/rest-management/invoice-management/invoice#get-invoice-detail)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `offset` | query | `string` | no |
| `sortby` | query | `string` | no |
| `invoiceNumber` | query | `string` | no |
| `customername` | query | `string` | no |
| `customerid` | query | `string` | no |
| `status` | query | `string` | no |
| `begindateat` | query | `date` | no |
| `enddateat` | query | `date` | no |
| `externalid` | query | `string` | no |
