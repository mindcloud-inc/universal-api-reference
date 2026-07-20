# Purchase Habitat Restoration with Ecologi

Purchases habitat restoration through Ecologi.

## Endpoint

- **Method:** `POST`
- **Path:** `/impact/habitat-restoration`
- **Base URL:** `https://public.ecologi.com`
- **Official documentation:** [Purchase Habitat Restoration](https://docs.ecologi.com/docs/public-api-docs/4e33697efbfdf-purchase-habitat-restoration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | body | `number` | yes | The number of square metres of habitat to restore. |
| `name` | body | `string` | no | Optional funded-by name shown with the purchase. |
| `test` | body | `boolean` | no | Optional advanced flag retained for Ecologi purchase requests. Current public Ecologi guidance does not clearly document sandbox semantics, and runtime validation still required billing details with this flag enabled. |
