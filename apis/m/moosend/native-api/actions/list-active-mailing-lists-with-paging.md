# List Active Mailing Lists With Paging with Moosend

Retrieves active mailing lists from Moosend with paging.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/{{Page}}/{{PageSize}}.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [List Active Mailing Lists With Paging](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54562-Get-all-active-mailing-lists-with-paging?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Page` | path | `number` | no | The page that you want to get. |
| `PageSize` | path | `number` | no | The number of email lists per page. |
| `SortBy` | query | `string` | no | The name of the email list property to sort results by. Possible values: Name , Subject , Status , DeliveredOn , and CreatedOn (Default). |
| `SortMethod` | query | `string` | no | Specifies the method to sort results. Possible values: DESC for descending and ASC (Default) for ascending. |
