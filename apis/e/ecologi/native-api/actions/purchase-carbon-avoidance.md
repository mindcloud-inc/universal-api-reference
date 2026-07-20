# Purchase Carbon Avoidance with Ecologi

Purchases carbon avoidance through Ecologi.

## Endpoint

- **Method:** `POST`
- **Path:** `/impact/carbon`
- **Base URL:** `https://public.ecologi.com`
- **Official documentation:** [Purchase Carbon Avoidance](https://docs.ecologi.com/docs/public-api-docs/e07bbee7fa605-purchase-carbon-avoidance)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | body | `number` | yes | The number of carbon avoidance units to purchase. |
| `units` | body | `list` | yes | The unit type for the purchase. Accepted values: `KG`, `Tonnes`. |
| `name` | body | `string` | no | Optional funded-by name shown with the purchase. |
| `test` | body | `boolean` | no | Optional advanced flag retained for Ecologi purchase requests. Current public Ecologi guidance does not clearly document sandbox semantics, and runtime validation still required billing details with this flag enabled. |
