# List Campaigns By Page And Page Size with Moosend

Retrieves campaigns from Moosend by page and page size.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/{{Page}}/{{PageSize}}.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [List Campaigns By Page And Page Size](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54585-Get-all-campaigns-by-page-and-page-size?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Page` | path | `number` | no | The page number to display results for. Returns the first page if not specified. |
| `PageSize` | path | `number` | no | The maximum number of results per page. This must be a positive integer up to 1000 . Returns 10 results per page if not specified. If a value greater than 1000 is specified, it is treated as 1000 . |
| `SortBy` | query | `string` | no | The name of the campaign property to sort results by. Possible values: Name , Subject , Status , DeliveredOn , and CreatedOn (Default). |
| `SortMethod` | query | `string` | no | Specifies the method to sort results. Possible values: DESC  for descending and  ASC (Default) for ascending. |
