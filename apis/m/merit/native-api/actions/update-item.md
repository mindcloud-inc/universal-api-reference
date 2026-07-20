# Update Item with Merit

## Endpoint

- **Method:** `POST`
- **Path:** `v1/updateitem`
- **Base URL:** `https://aktiva.merit.ee/api`
- **Official documentation:** [Update Item](https://api.merit.ee/connecting-robots/reference-manual/items/update-item/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Id` | body | `string` | yes | Item ID from Merit docs. |
| `Description` | body | `string` | no | Updated item description. |
