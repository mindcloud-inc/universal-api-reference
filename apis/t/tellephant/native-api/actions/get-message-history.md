# Get message history with Tellephant

Retrieves delivery history for a message in Tellephant.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/message-history`
- **Base URL:** `https://api.tellephant.com`
- **Official documentation:** [Get message history](https://app.tellephant.com/api-documentation#message-history)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | body | `string` | yes | Tellephant message ID to look up. |
