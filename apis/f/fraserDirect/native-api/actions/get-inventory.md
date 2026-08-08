# Get inventory with Fraser Direct

## Endpoint

- **Method:** `GET`
- **Path:** `/GetInventory`
- **Base URL:** `{baseURL}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `GroupByLot` | body | `list` | yes | Required. Use Y to group inventory by lot or N to aggregate across lots. Accepted values: `0`, `1`. |
| `IncludeInPick` | body | `list` | yes | Required. Use Y to include inventory currently in picking or N to exclude it. Accepted values: `0`, `1`. |
