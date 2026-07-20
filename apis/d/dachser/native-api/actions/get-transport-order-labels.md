# Get Transport Order Labels with Dachser

Retrieves labels for an existing transport order in Dachser.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/v2/transportorders/{id}/labels`
- **Base URL:** `https://api-gateway.dachser.com/`
- **Official documentation:** [Get Transport Order Labels](https://api-portal.dachser.com/bi.b2b.portal/api/library/transportorder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | DACHSER transport order ID. |
| `label-format` | query | `string` | no | Label format. Use P for PDF or Z for Zebra Printer Language. |
