# Send Message with Noor

Creates a message in a Noor thread.

## Endpoint

- **Method:** `POST`
- **Path:** `/sendMessage`
- **Base URL:** `https://sun.noor.to/api/v0`
- **Official documentation:** [Send Message](https://usenoor.notion.site/v0-e812ae5e5976420f81232fa1c0316e84)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | body | `string` | yes | Get this from Noor Settings > API. |
| `thread` | body | `string` | yes | Enter the exact Noor thread name. |
| `text` | body | `string` | yes | The message text. Markdown is supported. |
| `documentId` | body | `string` | no | Optional attached file ID uploaded with Noor's upload API. |
| `notifyByName[]` | body | `array<string>` | no | Optional Noor member names to notify, for example ["Ben"]. |
| `notifyById[]` | body | `array<string>` | no | Optional Noor member IDs to notify, for example ["User:123a"]. |
