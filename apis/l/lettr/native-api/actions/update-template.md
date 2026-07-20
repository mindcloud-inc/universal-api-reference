# Update Template with Lettr

## Endpoint

- **Method:** `PUT`
- **Path:** `/templates/:slug`
- **Base URL:** `https://app.lettr.com/api/`
- **Official documentation:** [Update Template](https://docs.lettr.com/api-reference/templates/update-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html` | body | `string` | no | Updated HTML content. |
| `name` | body | `string` | no | Updated template name. |
| `slug` | path | `string` | yes | Template slug. |
