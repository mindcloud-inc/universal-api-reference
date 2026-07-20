# Send Transport Order with Dachser

Sends an existing transport order to Dachser TMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/v2/transportorders/{id}/send`
- **Base URL:** `https://api-gateway.dachser.com/`
- **Official documentation:** [Send Transport Order](https://api-portal.dachser.com/bi.b2b.portal/api/library/transportorder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | DACHSER transport order ID. |
| `label-format` | query | `string` | no | Label format. Use P for PDF or Z for Zebra Printer Language. |
