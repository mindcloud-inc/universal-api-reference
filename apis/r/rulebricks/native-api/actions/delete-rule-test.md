# Delete Rule Test with Rulebricks

Deletes a test from a Rulebricks rule.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/admin/rules/:slug/tests/:testId`
- **Base URL:** `https://rulebricks.com/api/v1`
- **Official documentation:** [Delete Rule Test](https://rulebricks.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Unique slug of the rule whose test should be deleted |
| `testId` | path | `string` | yes | ID of the test to delete |
