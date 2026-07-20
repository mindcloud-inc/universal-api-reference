# Create Labels with Dachser

Creates shipping labels for a shipment in Dachser.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/v2/labels`
- **Base URL:** `https://api-gateway.dachser.com/`
- **Official documentation:** [Create Labels](https://api-portal.dachser.com/bi.b2b.portal/api/library/label)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `format` | body | `string` | no | Label format. Use P for PDF or Z for ZPL. |
| `count` | body | `number` | no | Number of labels to receive. Maximum 10. |
| `fontFileName` | body | `string` | no | Font file name for ZPL label format. |
| `shipment` | body | `object` | yes | Shipment data to render labels for. |
| `acceptLanguage` | query | `string` | no | Optional language sent as the Accept-Language header. |
