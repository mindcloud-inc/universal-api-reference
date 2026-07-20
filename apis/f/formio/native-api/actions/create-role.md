# Create Role with Form.io

Creates a new role in your Form.io project.

## Endpoint

- **Method:** `POST`
- **Path:** `/role`
- **Base URL:** `https://neabnzbnvbushtk.form.io`
- **Official documentation:** [Create Role](https://help.form.io/developers/introduction/api-documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `admin` | body | `boolean` | no | Whether the role is an admin role. |
| `default` | body | `boolean` | no | Whether the role is the default role. |
| `description` | body | `string` | no | Role description. |
| `title` | body | `string` | yes | Role title. |
