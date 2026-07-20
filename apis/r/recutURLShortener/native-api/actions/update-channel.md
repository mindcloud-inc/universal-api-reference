# Update Channel with Recut URL Shortener

Updates an existing channel in Recut URL Shortener.

## Endpoint

- **Method:** `PUT`
- **Path:** `/channel/:id/update`
- **Base URL:** `https://app.recut.in/api`
- **Official documentation:** [Update Channel](https://app.recut.in/developers#update-channel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Channel ID. |
| `name` | body | `string` | yes | Channel name. |
| `description` | body | `string` | no | Channel description. |
| `color` | body | `string` | no | Channel badge color in hex format. |
| `starred` | body | `boolean` | no | Whether the channel is starred. |
