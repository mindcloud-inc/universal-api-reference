# Create Item Group with Merit

## Endpoint

- **Method:** `POST`
- **Path:** `v2/senditemgroups`
- **Base URL:** `https://aktiva.merit.ee/api`
- **Official documentation:** [Create Item Group](https://api.merit.ee/connecting-robots/reference-manual/items/add-item-groups/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ItemGroups[]` | body | `array<object>` | yes | Array of item-group objects to create. |
