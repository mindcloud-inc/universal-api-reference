# Create Recipient with updown.io

Creates a new alert recipient in updown.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/recipients`
- **Base URL:** `https://updown.io/api`
- **Official documentation:** [Create Recipient](https://updown.io/api#POST-/api/recipients)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Optional label for recipient types that support it. |
| `selected` | body | `boolean` | no | Whether the new recipient is selected on all existing checks. |
| `type` | body | `list` | yes | Recipient type: email, sms, webhook, slack_compatible, or msteams. Accepted values: `email`, `msteams`, `slack_compatible`, `sms`, `webhook`. |
| `value` | body | `string` | yes | The recipient value, such as an email address, phone number, or URL. |
