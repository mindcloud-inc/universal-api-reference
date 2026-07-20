# Move Contact To List with Reply

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/Actions/moveContactsToLists`
- **Base URL:** `https://api.reply.io`
- **Official documentation:** [Move Contact To List](https://apidocs.reply.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ContactIds[]` | body | `array<number>` | yes | Reply contact IDs to move. |
| `ListIds[]` | body | `array<number>` | yes | Reply list IDs to receive the contacts. |
