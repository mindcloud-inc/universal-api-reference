# Update Meeting Notes with IceCubes

## Endpoint

- **Method:** `PUT`
- **Path:** `/meetings/:id/notes`
- **Base URL:** `https://icecubes.app/api/public`
- **Official documentation:** [Update Meeting Notes](https://icecubes.app/docs/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The meeting ID to update notes for. |
| `content` | body | `string` | yes | The notes content to save. |
