# List Notes with Toodledo

Retrieves notes from Toodledo.

## Endpoint

- **Method:** `GET`
- **Path:** `/notes/get.php`
- **Base URL:** `https://api.toodledo.com/3`
- **Official documentation:** [List Notes](https://api.toodledo.com/3/notes/index.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before` | query | `number` | no | Return only notes modified before this GMT Unix timestamp. |
| `after` | query | `number` | no | Return only notes modified after this GMT Unix timestamp. |
| `id` | query | `number` | no | Fetch a single note by its numeric Toodledo note ID. |
| `start` | query | `number` | no | Number of records to skip before returning results. |
| `num` | query | `number` | no | Maximum number of notes to return. Toodledo documents a default and max of 1000. |
