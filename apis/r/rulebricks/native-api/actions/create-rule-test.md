# Create Rule Test with Rulebricks

Creates a test for a Rulebricks rule.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/rules/:slug/tests`
- **Base URL:** `https://rulebricks.com/api/v1`
- **Official documentation:** [Create Rule Test](https://rulebricks.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `critical` | body | `boolean` | yes | Whether the test is critical |
| `name` | body | `string` | yes | Name of the test |
| `request` | body | `object` | yes | Request object for the test |
| `response` | body | `object` | yes | Expected response object for the test |
| `slug` | path | `string` | yes | Unique slug of the rule that will receive the new test |
