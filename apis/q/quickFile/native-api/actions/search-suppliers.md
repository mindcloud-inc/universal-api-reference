# Search Suppliers with QuickFile

## Endpoint

- **Method:** `POST`
- **Path:** `/supplier/search`
- **Base URL:** `https://api.quickfile.co.uk/1_2`
- **Official documentation:** [Search Suppliers](https://api.quickfile.co.uk/d/v1_2/Supplier_Search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CompanyName` | body | `string` | no | Whole or partial supplier company name |
| `ContactName` | body | `string` | no | Whole or partial supplier contact name |
| `Email` | body | `string` | no | Whole or partial supplier email address |
| `Offset` | body | `number` | yes | Page offset for supplier results |
| `OrderDirection` | body | `string` | yes | Direction used to order supplier results |
| `OrderResultsBy` | body | `string` | yes | Field used to order supplier results |
| `ReturnCount` | body | `number` | yes | Maximum number of suppliers to return |
