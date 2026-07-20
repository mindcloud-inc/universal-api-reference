# Update Account with AltText.Ai

Updates your account settings in AltText.Ai.

## Endpoint

- **Method:** `PUT`
- **Path:** `/account`
- **Base URL:** `https://alttext.ai/api/v1`
- **Official documentation:** [Update Account](https://alttext.ai/apidocs#tag/Account/operation/update-account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Update the account name. |
| `notification_email` | body | `string` | no | Set the email address for important account notifications. |
| `webhook_url` | body | `string` | no | Set the default webhook URL for account notifications. |
