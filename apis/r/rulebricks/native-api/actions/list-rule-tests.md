# List Rule Tests with Rulebricks

Retrieves tests for a Rulebricks rule.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/rules/:slug/tests`
- **Base URL:** `https://rulebricks.com/api/v1`
- **Official documentation:** [List Rule Tests](https://rulebricks.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Unique slug of the rule whose tests should be listed |
