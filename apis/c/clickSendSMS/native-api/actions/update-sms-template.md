# Update SMS Template with ClickSend SMS

Updates an existing SMS template in ClickSend SMS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/sms/templates/:template_id`
- **Base URL:** `https://rest.clicksend.com`
- **Official documentation:** [Update SMS Template](https://developers.clicksend.com/docs/messaging/sms/other/update-sms-template/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `template_id` | path | `string` | yes |
| `template_name` | body | `string` | no |
| `body` | body | `string` | no |
