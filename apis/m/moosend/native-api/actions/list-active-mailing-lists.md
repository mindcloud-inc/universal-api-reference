# List Active Mailing Lists with Moosend

Retrieves active mailing lists from Moosend.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [List Active Mailing Lists](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54568-Get-all-active-mailing-lists?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `WithStatistics` | query | `string` | no | Specifies whether to fetch statistics for the subscribers. Possible values: true (Default) and false . |
| `SortBy` | query | `string` | no | The name of the email list property to sort results by. Possible values: Name , Subject , Status , DeliveredOn , and CreatedOn (Default). |
| `SortMethod` | query | `string` | no | Specifies the method to sort results. Possible values: DESC for descending and ASC (Default) for ascending. |
