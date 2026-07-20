# Get Enterprise Tree Count by Month with Digital Humani

Retrieves an enterprise's monthly tree count from Digital Humani.

## Endpoint

- **Method:** `GET`
- **Path:** `/enterprise/:id/treeCount/:month`
- **Base URL:** `https://api.digitalhumani.com`
- **Official documentation:** [Get Enterprise Tree Count by Month](https://docs.digitalhumani.com/#apitree_get_enterprise_month)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `month` | path | `string` | yes | Month in YYYY-MM format. |
