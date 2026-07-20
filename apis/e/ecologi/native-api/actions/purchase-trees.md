# Purchase Trees with Ecologi

Purchases trees through Ecologi.

## Endpoint

- **Method:** `POST`
- **Path:** `/impact/trees`
- **Base URL:** `https://public.ecologi.com`
- **Official documentation:** [Purchase Trees](https://docs.ecologi.com/docs/public-api-docs/004342d262f93-purchase-trees)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | body | `number` | yes | The number of trees to purchase. |
| `name` | body | `string` | no | Optional funded-by name shown with the purchased trees. |
| `test` | body | `boolean` | no | Optional advanced flag retained for Ecologi purchase requests. Current public Ecologi guidance does not clearly document sandbox semantics, and runtime validation still required billing details with this flag enabled. |
