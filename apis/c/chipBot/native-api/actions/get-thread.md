# Get Thread with ChipBot

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/connect/accounts/:accountId/domains/:domainId/kb-tree/:parentId`
- **Base URL:** `https://getchipbot.com`
- **Official documentation:** [Get Thread](https://getchipbot.com/api-docs/chat-api/get-a-thread)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parentId` | path | `string` | yes | Thread identifier returned on incoming chat payloads. |
