# Prepare Invoice from Shipment with Acumatica

## Endpoint

- **Method:** `POST`
- **Path:** `/entity/{endpointName}/{endpointVersion}/Shipment/PrepareInvoice`
- **Base URL:** `{uRL}`
- **Official documentation:** [Prepare Invoice from Shipment](https://help.acumatica.com/Wiki/ShowWiki.aspx?PageID=91dda8ed-5e92-48a5-a176-9a255506d0d6&wikiname=HelpRoot_Dev_Integration)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `entity` | body | `object` | no |
| `entity.ShipmentNbr` | body | `object` | no |
| `entity.ShipmentNbr.value` | body | `string` | yes |
