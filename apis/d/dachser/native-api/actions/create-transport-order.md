# Create Transport Order with Dachser

Creates a new transport order in Dachser.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/v2/transportorders/{basket}`
- **Base URL:** `https://api-gateway.dachser.com/`
- **Official documentation:** [Create Transport Order](https://api-portal.dachser.com/bi.b2b.portal/api/library/transportorder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `basket` | path | `string` | yes | Transport order basket. |
| `transportDate` | body | `date` | yes | Date when the goods shall be picked up. |
| `division` | body | `string` | yes | DACHSER division. Use T for industrial goods or F for food. |
| `product` | body | `string` | yes | DACHSER product code. |
| `term` | body | `string` | yes | Terms of delivery for European Logistics. |
| `consignee` | body | `object` | yes | Receiver of the consignment. |
| `transportOrderLines[]` | body | `array<object>` | yes | Detailed goods lines to be transported. |
| `labelFormat` | body | `string` | no | Label format. Use P for PDF or Z for ZPL. |
| `forwarder` | body | `object` | no | DACHSER branch that collects and dispatches the consignment. |
| `consignor` | body | `object` | no | Sender or pickup customer. |
| `transportOptions` | body | `object` | no | Optional DACHSER transport options. |
| `goodsValueInsurance` | body | `object` | no | Goods value insurance amount. |
| `references[]` | body | `array<object>` | no | Customer order, delivery note, and other references. |
| `furtherAddresses[]` | body | `array<object>` | no | Optional loading points, cover addresses, and other addresses. |
| `packingAids[]` | body | `array<object>` | no | Optional packing aids. |
| `texts[]` | body | `array<object>` | no | Additional texts for driver, invoice, or delivery note. |
| `orderGroup` | body | `string` | no | Order group for invoice splitting. |
