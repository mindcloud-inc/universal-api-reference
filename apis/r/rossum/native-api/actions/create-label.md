# Create Label with Rossum

Creates a new label in Rossum.

## Endpoint

- **Method:** `POST`
- **Path:** `/labels`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Create Label](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Text of the label. |
| `organization` | body | `string` | yes | Organization URL that owns the label. |
| `color` | body | `string` | no | Optional RGB hex color for the label. |
