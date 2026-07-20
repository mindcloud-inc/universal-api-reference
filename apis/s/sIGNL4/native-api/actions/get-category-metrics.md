# Get Category Metrics with SIGNL4

Retrieves category metrics from SIGNL4.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/categories/{teamId}/{categoryId}/metrics`
- **Base URL:** `https://connect.signl4.com/api`
- **Official documentation:** [Get Category Metrics](https://connect.signl4.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | ID of the team the category belongs to |
| `categoryId` | path | `string` | yes | ID of the category to get |
