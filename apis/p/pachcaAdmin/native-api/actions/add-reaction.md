# Add Reaction with Pachca (Admin)

Creates a new reaction in the Pachca Admin API.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/:id/reactions`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [Add Reaction](https://dev.pachca.com/api/reactions/add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Pachca message ID. |
| `code` | body | `string` | yes | Reaction emoji glyph, for example 👍. Pachca rejects text aliases like thumbsup. |
| `name` | body | `string` | no | — |
