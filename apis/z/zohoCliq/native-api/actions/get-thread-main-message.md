# Get Thread Main Message with Zoho Cliq

Retrieves the main message of a Zoho Cliq thread.

## Endpoint

- **Method:** `GET`
- **Path:** `/threads/:threadChatId/messages/main`
- **Base URL:** `https://cliq.zoho.com/api/v2`
- **Official documentation:** [Get Thread Main Message](https://www.zoho.com/cliq/help/restapi/v2/#get-main-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `threadChatId` | path | `string` | yes | The chat ID of the thread whose main message should be retrieved. |
