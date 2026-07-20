# Unassign Label from Supplier with Recommand

Removes a label from a Recommand supplier.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/suppliers/:supplierId/labels/:labelId`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Unassign Label from Supplier](https://recommand.eu/en/reference/suppliers/unassign-label-from-supplier)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `labelId` | path | `string` | yes | labelId parameter. |
| `supplierId` | path | `string` | yes | supplierId parameter. |
