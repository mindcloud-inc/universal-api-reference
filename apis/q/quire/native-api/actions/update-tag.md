# Update Tag with Quire

Updates an existing tag in Quire.

## Endpoint

- **Method:** `PUT`
- **Path:** `tag/:oid`
- **Base URL:** `https://quire.io/api`
- **Official documentation:** [Update Tag](https://quire.io/dev/api/#operation--tag--oid--put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `oid` | path | `string` | yes | The Quire tag OID. |
| `name` | body | `string` | no | The updated display name for the tag. |
| `color` | body | `string` | no | Optional updated Quire color code such as 35. |
| `global` | body | `boolean` | no | Whether the tag should be available across projects. |
| `project` | body | `string` | no | Project OID used only when global is explicitly false. |
