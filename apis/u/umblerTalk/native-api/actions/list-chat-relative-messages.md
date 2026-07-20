# List Chat Relative Messages with Umbler Talk

Retrieves chat messages around a selected date in Umbler Talk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/chats/[:chatId]/relative-messages/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [List Chat Relative Messages](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | path | `string` | yes | The chat ID. |
| `Direction` | query | `string` | yes | Relative message direction. |
| `FromEventUTC` | query | `date` | yes | Start date/time for relative messages. |
| `organizationId` | query | `string` | yes | The organization ID. |
| `Take` | query | `number` | yes | Number of messages to retrieve. |
