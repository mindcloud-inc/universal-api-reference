# Purchase Carbon Removals with Ecologi

Purchases carbon removals through Ecologi.

## Endpoint

- **Method:** `POST`
- **Path:** `/impact/carbon-removal`
- **Base URL:** `https://public.ecologi.com`
- **Official documentation:** [Purchase Carbon Removals](https://docs.ecologi.com/docs/public-api-docs/f65cbeae299f9-purchase-carbon-removals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | body | `number` | yes | The number of kilograms of carbon removal to purchase. |
| `name` | body | `string` | no | Optional funded-by name shown with the purchase. |
| `test` | body | `boolean` | no | Optional advanced flag retained for Ecologi purchase requests. Current public Ecologi guidance does not clearly document sandbox semantics, and runtime validation still required billing details with this flag enabled. |
