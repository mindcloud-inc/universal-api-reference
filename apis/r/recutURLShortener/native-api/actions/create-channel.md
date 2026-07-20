# Create Channel with Recut URL Shortener

Creates a channel in Recut URL Shortener.

## Endpoint

- **Method:** `POST`
- **Path:** `/channel/add`
- **Base URL:** `https://app.recut.in/api`
- **Official documentation:** [Create Channel](https://app.recut.in/developers#create-a-channel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Channel name. |
| `description` | body | `string` | no | Channel description. |
| `color` | body | `string` | no | Channel badge color in hex format. |
| `starred` | body | `boolean` | no | Whether the channel is starred. |
