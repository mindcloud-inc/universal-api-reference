# Send Email by Tags with SendMe

## Endpoint

- **Method:** `POST`
- **Path:** `/api/messages/email/tags`
- **Base URL:** `https://app.sendme123.com`
- **Official documentation:** [Send Email by Tags](https://docs.sendme123.com/en/api/messages/email-tags/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | Email content. |
| `subject` | body | `string` | yes | Email subject. |
| `tagIds[]` | body | `array<string>` | yes | List of tag IDs. |
