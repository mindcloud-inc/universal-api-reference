# Create SMS Template with NobelSMS

Creates a new SMS template in NobelSMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/sms_template`
- **Base URL:** `https://api.nobelsms.com/rest`
- **Official documentation:** [Create SMS Template](https://api.nobelsms.com/rest/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | no | Template content. |
| `name` | body | `string` | yes | Template name. |
| `sender_id` | body | `string` | no | Sender ID. |
