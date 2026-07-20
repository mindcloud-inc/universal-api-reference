# Update SMS Template with NobelSMS

Updates an existing SMS template in NobelSMS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/sms_template/:id`
- **Base URL:** `https://api.nobelsms.com/rest`
- **Official documentation:** [Update SMS Template](https://api.nobelsms.com/rest/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | no | Template content. |
| `id` | path | `number` | yes | Template ID. |
| `name` | body | `string` | no | Template name. |
| `sender_id` | body | `string` | no | Sender ID. |
