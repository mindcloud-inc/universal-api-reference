# Import Rule with Rulebricks

Creates or updates a rule in Rulebricks.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/rules/import`
- **Base URL:** `https://rulebricks.com/api/v1`
- **Official documentation:** [Import Rule](https://rulebricks.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rule` | body | `object` | yes | Rule object accepted by the Rulebricks import endpoint |
