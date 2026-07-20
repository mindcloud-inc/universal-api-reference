# Bulk Quote Actions with Invoice Ninja

## Endpoint

- **Method:** `POST`
- **Path:** `/quotes/bulk`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [Bulk Quote Actions](https://api-docs.invoicing.co/#tag/quotes/operation/bulkQuotes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | body | `string` | yes | Bulk quote action such as approve, convert, send_email, mark_sent, restore, delete, or archive. |
| `ids[]` | body | `array<string>` | yes | Array of quote IDs for the bulk action. |
