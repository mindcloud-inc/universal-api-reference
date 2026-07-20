# Update Form with Form.io

Updates an existing form in your Form.io project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/form/:id`
- **Base URL:** `https://neabnzbnvbushtk.form.io`
- **Official documentation:** [Update Form](https://help.form.io/developers/introduction/api-documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `display` | body | `string` | no | Updated form display mode. |
| `id` | path | `string` | yes | The Form.io form ID. |
| `name` | body | `string` | no | Updated internal form name. |
| `path` | body | `string` | no | Updated public form path slug. |
| `title` | body | `string` | no | Updated form title. |
| `type` | body | `string` | no | Updated form type. |
