# List Message Log with MojoTxt

Retrieves a message log from MojoTxt.

## Endpoint

- **Method:** `GET`
- **Path:** `/:phoneNumber/messageLog/list`
- **Base URL:** `https://app.mojotxt.com/api/v1`
- **Official documentation:** [List Message Log](https://app.mojotxt.com/api/docs/v1/messagelog.php#list)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Direction` | query | `string` | no | Filter the log to incoming (I) or outgoing (O) messages. |
| `EndTime` | query | `string` | no | Show messages older than this UNIX timestamp. |
| `MessageID` | query | `string` | no | Show log entries for a specific subscription-list message. |
| `phoneNumber` | path | `string` | yes | The MojoTxt phone number in international format, like +17792533748. |
| `StartTime` | query | `string` | no | Show messages newer than this UNIX timestamp. |
