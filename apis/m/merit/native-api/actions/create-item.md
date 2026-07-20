# Create Item with Merit

## Endpoint

- **Method:** `POST`
- **Path:** `v2/senditems`
- **Base URL:** `https://aktiva.merit.ee/api`
- **Official documentation:** [Create Item](https://api.merit.ee/connecting-robots/reference-manual/items/add-items/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Items[]` | body | `array<object>` | yes | Array of item objects to create. |
