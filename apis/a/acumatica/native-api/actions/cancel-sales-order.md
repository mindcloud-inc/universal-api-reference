# Cancel Sales Order with Acumatica

## Endpoint

- **Method:** `POST`
- **Path:** `/entity/{endpointName}/{endpointVersion}/SalesOrder/CancelSalesOrder`
- **Base URL:** `{uRL}`
- **Official documentation:** [Cancel Sales Order](https://help.acumatica.com/Wiki/ShowWiki.aspx?PageID=91dda8ed-5e92-48a5-a176-9a255506d0d6&wikiname=HelpRoot_Dev_Integration)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `entity` | body | `object` | no |
| `entity.OrderType` | body | `object` | no |
| `entity.OrderType.value` | body | `string` | yes |
| `entity.OrderNbr` | body | `object` | no |
| `entity.OrderNbr.value` | body | `string` | yes |
