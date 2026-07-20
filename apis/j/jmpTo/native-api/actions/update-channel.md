# Update Channel with JmpTo

Updates an existing channel in JmpTo.

## Endpoint

- **Method:** `PUT`
- **Path:** `/channel/:id/update`
- **Base URL:** `https://jmpto.net/api`
- **Official documentation:** [Update Channel](https://jmpto.net/developers#update-channel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Channel ID to update. |
| `name` | body | `string` | no | Channel name. |
| `description` | body | `string` | no | Channel description. |
| `color` | body | `string` | no | Channel badge color in HEX format. |
| `starred` | body | `boolean` | no | Whether to star the channel. |
