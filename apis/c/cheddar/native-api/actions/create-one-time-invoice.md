# Create One-Time Invoice with Cheddar

Creates a one-time invoice in Cheddar.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices/new/productCode/{productCode}/code/:customerCode`
- **Base URL:** `https://getcheddar.com/xml`
- **Official documentation:** [Create One-Time Invoice](https://docs.getcheddar.com/#create-a-one-time-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Customer code from Cheddar. |
| `charges[<user-defined>]` | body | `list<object>` | yes | Charge rows to include on the one-time invoice. |
| `charges[<user-defined>][chargeCode]` | body | `string` | yes | Charge code for one invoice line. |
| `charges[<user-defined>][quantity]` | body | `number` | yes | Positive integer quantity for one invoice line. |
| `charges[<user-defined>][eachAmount]` | body | `number` | yes | Positive or negative amount with two-digit decimal precision for one invoice line. |
| `charges[<user-defined>][description]` | body | `string` | no | Description for one invoice line. |
| `remoteAddress` | body | `string` | no | Client IPv4 address for fraud protection and rate limiting. |
