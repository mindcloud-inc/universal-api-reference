# Update Template with ApproveThis

Updates an existing approval template in ApproveThis.

## Endpoint

- **Method:** `PUT`
- **Path:** `/templates/:template`
- **Base URL:** `https://app.approvethis.com/api/v1`
- **Official documentation:** [Update Template](https://app.approvethis.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template` | path | `string` | yes | The template slug. |
| `name` | body | `string` | yes | The template name. |
| `slug` | body | `string` | yes | A unique template slug. |
| `description` | body | `string` | no | An optional template description. |
