# Create Template V3 with E2B

Creates a new template in E2B.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/templates`
- **Base URL:** `https://api.e2b.app`
- **Official documentation:** [Create Template V3](https://e2b.dev/docs/api-reference/templates/create-template-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Name of the template. Can include a tag with colon separator. |
| `tags[]` | body | `array<string>` | no | Tags to assign to the template build. |
