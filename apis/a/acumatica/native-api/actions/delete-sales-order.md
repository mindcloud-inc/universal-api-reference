# Delete Sales Order with Acumatica

## Endpoint

- **Method:** `DELETE`
- **Path:** `/entity/{endpointName}/{endpointVersion}/SalesOrder/:id`
- **Base URL:** `{uRL}`
- **Official documentation:** [Delete Sales Order](https://help.acumatica.com/Wiki/ShowWiki.aspx?PageID=91dda8ed-5e92-48a5-a176-9a255506d0d6&wikiname=HelpRoot_Dev_Integration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Acumatica Sales Order entity GUID returned in the record's id field. |
