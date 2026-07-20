# Search Invoices with QuickFile

## Endpoint

- **Method:** `POST`
- **Path:** `/invoice/search`
- **Base URL:** `https://api.quickfile.co.uk/1_2`
- **Official documentation:** [Search Invoices](https://api.quickfile.co.uk/d/v1_2/Invoice_Search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ReturnCount` | body | `number` | no | How many invoices to return, up to 200. |
| `Offset` | body | `number` | no | Page offset starting at 0. |
| `OrderResultsBy` | body | `string` | no | Field used to order invoice search results. |
| `OrderDirection` | body | `string` | no | Order direction for invoice search results. |
| `ClientName` | body | `string` | no | Whole or part of the client company name. |
| `IssueDateFrom` | body | `date` | no | Issued date range start. |
| `IssueDateTo` | body | `date` | no | Issued date range end. |
| `AmountFrom` | body | `number` | no | Minimum invoice amount. |
| `AmountTo` | body | `number` | no | Maximum invoice amount. |
| `Status` | body | `string` | no | Invoice status to search. |
