# Update email settings for the logged-in user with Maildrip

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/users/email-settings`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Update email settings for the logged-in user](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `emailFrom` | body | `string` | no |
| `emailReplyTo` | body | `string` | no |
