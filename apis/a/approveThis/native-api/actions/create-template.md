# Create Template with ApproveThis

Creates a new approval template in ApproveThis.

## Endpoint

- **Method:** `POST`
- **Path:** `/templates`
- **Base URL:** `https://app.approvethis.com/api/v1`
- **Official documentation:** [Create Template](https://app.approvethis.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The template name. |
| `slug` | body | `string` | yes | A unique template slug. |
| `description` | body | `string` | no | An optional template description. |
