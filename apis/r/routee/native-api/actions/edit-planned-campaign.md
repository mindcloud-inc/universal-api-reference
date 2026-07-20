# Edit planned campaign with Routee

Updates an existing planned campaign in Routee.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/campaigns`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Edit planned campaign](https://docs.routee.net/reference/editing-planned-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | ID of the created campaign |
| `name` | query | `string` | no | Campaign name |
| `senderName` | query | `string` | no | Sender name |
| `senderEmail` | query | `string` | no | Sender email address |
| `subject` | query | `string` | no | Email subject |
| `body` | query | `string` | no | HTML code of template, encoded in base64 |
| `templateId` | query | `string` | no | ID of the template uploaded in the service. Use this method to get the template ID (use either real_id or id parameter from the reply) |
| `sendDate` | query | `string` | no | Date of the scheduled email campaign (optional parameter) must fit the following format: Y-m-d H:i:s (for example: 2016-02-02 23:34:23) and can not be less than the current date and time |
