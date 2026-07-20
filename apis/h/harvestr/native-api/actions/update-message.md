# Update Message with Harvestr.io

## Endpoint

- **Method:** `PATCH`
- **Path:** `/message/{id}`
- **Base URL:** `https://rest.harvestr.io/v1`
- **Official documentation:** [Update Message](https://developers.harvestr.io/api/update-a-message/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier (id or clientId) |
| `labels` | body | `object` | no | Message labels. Priority order: 1) 'set' overwrites all labels, 2) 'connect' and 'disconnect' are applied together (if a label is in both, disconnect takes precedence and it won't be connected) |
| `labels.connect[]` | body | `array<string>` | no | Connect a list of message labels |
| `labels.disconnect[]` | body | `array<string>` | no | Disconnect a list of message labels |
| `labels.set[]` | body | `array<string>` | no | Set and overwrite a list of message labels |
| `inboxType` | body | `string` | no | Message inbox type. NEW = unprocessed inbox, PROCESSED = processed inbox, BIN = archived/trash |
