# Client Statement PDF with Invoice Ninja

## Endpoint

- **Method:** `POST`
- **Path:** `/client_statement`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [Client Statement PDF](https://api-docs.invoicing.co/#tag/clients/operation/clientStatement)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | body | `string` | yes | Start date for the statement period in Y-m-d format. |
| `end_date` | body | `string` | yes | End date for the statement period in Y-m-d format. |
| `client_id` | body | `string` | yes | Hashed client ID for the statement. |
| `show_payments_table` | body | `boolean` | no | Whether to include the payments table in the PDF. |
| `show_credits_table` | body | `boolean` | no | Whether to include the credits table in the PDF. |
| `show_aging_table` | body | `boolean` | no | Whether to include the aging table in the PDF. |
