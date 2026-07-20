# Create a campaign with Routee

Creates a new campaign in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Create a campaign](https://docs.routee.net/reference/creating-a-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `senderName` | query | `string` | no | Sender name |
| `senderEmail` | query | `string` | no | Sender email address |
| `subject` | query | `string` | no | Email subject |
| `body` | query | `string` | no | The email body, encoded in base64 |
| `listId` | query | `string` | no | Mailing list ID |
| `name` | query | `string` | no | Campaign name (an optional parameter) |
| `type` | query | `string` | no | Possible value - "draft" (a newsletter will be created as a draft). An optional parameter. |
| `attachments` | query | `string` | no | Attached files, a serialized array in which the key is the name of the attachment, and the value is the content of the attachment (an optional parameter) |
