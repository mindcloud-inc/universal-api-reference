# Confirm Shipment with Acumatica

## Endpoint

- **Method:** `PUT`
- **Path:** `/entity/{endpointName}/{endpointVersion}/Shipment/ConfirmShipment`
- **Base URL:** `{uRL}`
- **Official documentation:** [Confirm Shipment](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ShipmentNbr` | body | `object` | no |
| `ShipmentNbr.value` | body | `string` | no |
