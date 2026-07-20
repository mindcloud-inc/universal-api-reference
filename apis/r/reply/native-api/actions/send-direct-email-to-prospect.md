# Send Direct Email To Prospect with Reply

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/prospects/:prospectid/emails`
- **Base URL:** `https://api.reply.io`
- **Official documentation:** [Send Direct Email To Prospect](https://apidocs.reply.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | yes | Email body content. |
| `emailAccountId` | body | `number` | no | Email account to use for sending the email. |
| `prospectid` | path | `number` | yes | Reply prospect identifier. |
| `subject` | body | `string` | yes | Email subject line. |
