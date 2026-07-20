# Search Clients with QuickFile

## Endpoint

- **Method:** `POST`
- **Path:** `/client/search`
- **Base URL:** `https://api.quickfile.co.uk/1_2`
- **Official documentation:** [Search Clients](https://api.quickfile.co.uk/d/v1_2/Client_Search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CompanyName` | body | `string` | no | Whole or partial client company name |
| `ContactName` | body | `string` | no | Whole or partial client contact name |
| `Email` | body | `string` | no | Whole or partial client email address |
| `Offset` | body | `number` | yes | Page offset for client results |
| `OrderDirection` | body | `string` | yes | Direction used to order client results |
| `OrderResultsBy` | body | `string` | yes | Field used to order client results |
| `ReturnCount` | body | `number` | yes | Maximum number of clients to return |
