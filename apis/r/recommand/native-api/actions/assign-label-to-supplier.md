# Assign Label to Supplier with Recommand

Assigns a label to a Recommand supplier.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/suppliers/:supplierId/labels/:labelId`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Assign Label to Supplier](https://recommand.eu/en/reference/suppliers/assign-label-to-supplier)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `labelId` | path | `string` | yes | labelId parameter. |
| `supplierId` | path | `string` | yes | supplierId parameter. |
