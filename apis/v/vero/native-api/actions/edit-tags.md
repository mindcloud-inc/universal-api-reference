# Edit Tags with Vero

Updates a user's tags in Vero.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/users/tags/edit`
- **Base URL:** `https://api.getvero.com`
- **Official documentation:** [Edit Tags](https://help.getvero.com/api-reference/tags/edit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The unique identifier of the user whose tags should be edited. |
| `add[]` | body | `array<string>` | no | Optional list of tags to add to the user. |
| `remove[]` | body | `array<string>` | no | Optional list of tags to remove from the user. |
