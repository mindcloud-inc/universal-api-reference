# Update Role with Form.io

Updates an existing role in your Form.io project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/role/:id`
- **Base URL:** `https://neabnzbnvbushtk.form.io`
- **Official documentation:** [Update Role](https://help.form.io/developers/introduction/api-documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `admin` | body | `boolean` | no | Whether the role is an admin role. |
| `default` | body | `boolean` | no | Whether the role is the default role. |
| `description` | body | `string` | no | Updated role description. |
| `id` | path | `string` | yes | The Form.io role ID. |
| `title` | body | `string` | no | Updated role title. |
