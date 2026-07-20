# Update Chat with FuseDesk

Updates an existing chat in FuseDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/chats/:chatId`
- **Base URL:** `https://{appName}.fusedesk.com`
- **Official documentation:** [Update Chat](https://documenter.getpostman.com/view/11014835/SztBc8ix#04842f72-4833-46c1-bd1a-b4213a0e008d)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `caseId` | body | `number` | no | Related case ID. |
| `chatId` | path | `string` | yes | The FuseDesk chat ID. |
| `clientName` | body | `string` | no | Client display name. |
| `contactUuid` | body | `string` | no | Associated contact UUID. |
| `departmentId` | body | `number` | no | Assigned department ID. |
| `repId` | body | `number` | no | Assigned rep user ID. |
| `title` | body | `string` | no | Chat title. |
| `unseen` | body | `number` | no | Unseen message count. |
