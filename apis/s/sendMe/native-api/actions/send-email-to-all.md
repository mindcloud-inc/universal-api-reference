# Send Email to All with SendMe

## Endpoint

- **Method:** `POST`
- **Path:** `/api/messages/email/all`
- **Base URL:** `https://app.sendme123.com`
- **Official documentation:** [Send Email to All](https://docs.sendme123.com/en/api/messages/email-all/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | Email content. |
| `subject` | body | `string` | yes | Email subject. |
