# Create Editor Session with Stencil

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/editor/sessions`
- **Base URL:** `https://api.usestencil.com`
- **Official documentation:** [Create Editor Session](https://docs.usestencil.com/api/endpoints/editor-session#create-a-new-session)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `expires` | body | `number` | yes | Time until expiration in seconds. |
| `name` | body | `string` | yes | Name of the editor session. |
| `permissions` | body | `object` | no | Optional permissions object for the editor session. |
| `template_id` | body | `string` | yes | Template ID to give edit access to. |
