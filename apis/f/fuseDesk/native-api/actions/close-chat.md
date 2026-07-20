# Close Chat with FuseDesk

Closes an existing chat in FuseDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/chats/:chatId/close`
- **Base URL:** `https://{appName}.fusedesk.com`
- **Official documentation:** [Close Chat](https://documenter.getpostman.com/view/11014835/SztBc8ix#fda44692-6a99-4b38-8d98-408bdbeca27f)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | path | `string` | yes | The FuseDesk chat ID. |
| `depid` | body | `number` | no | Assigned department ID. |
| `repid` | body | `number` | no | Assigned rep user ID. |
| `status` | body | `string` | no | Chat close status. |
