# Connect Sender Profile With GoLogin with GetSales.io

## Endpoint

- **Method:** `POST`
- **Path:** `/flows/client-api/sender-profiles/connect-external`
- **Base URL:** `https://amazing.getsales.io`
- **Official documentation:** [Connect Sender Profile With GoLogin](https://api.getsales.io/api/openapi/sender-profiles/connectsenderprofile.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | First name of the sender. |
| `last_name` | body | `string` | yes | Last name of the sender. |
| `label` | body | `string` | no | Optional custom label for identification. |
| `gologin_external_id` | body | `string` | yes | External ID from GoLogin used to create the browser profile. |
| `schedule` | body | `object` | no | Schedule object with timezone and timeblocks. |
| `smart_limits_enabled` | body | `boolean` | no | Enables smart limits for automation. |
| `notification_emails[]` | body | `array<string>` | no | Notification email addresses. |
| `browser_owner` | body | `string` | no | Optional owner of the browser profile. |
