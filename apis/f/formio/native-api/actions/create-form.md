# Create Form with Form.io

Creates a new form in your Form.io project.

## Endpoint

- **Method:** `POST`
- **Path:** `/form`
- **Base URL:** `https://neabnzbnvbushtk.form.io`
- **Official documentation:** [Create Form](https://help.form.io/developers/introduction/api-documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `display` | body | `string` | no | Form display mode. |
| `name` | body | `string` | yes | Internal form name. |
| `path` | body | `string` | yes | Public form path slug. |
| `title` | body | `string` | yes | Human-readable form title. |
| `type` | body | `string` | no | Form type such as form or resource. |
