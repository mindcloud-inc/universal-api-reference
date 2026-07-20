# Create Channel with JmpTo

Creates a channel in JmpTo.

## Endpoint

- **Method:** `POST`
- **Path:** `/channel/add`
- **Base URL:** `https://jmpto.net/api`
- **Official documentation:** [Create Channel](https://jmpto.net/developers#create-a-channel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Channel name. |
| `description` | body | `string` | no | Channel description. |
| `color` | body | `string` | no | Channel badge color in HEX format. |
| `starred` | body | `boolean` | no | Whether to star the channel. |
