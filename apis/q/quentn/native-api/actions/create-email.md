# Create Email with Quentn

## Endpoint

- **Method:** `POST`
- **Path:** `/mail/add`
- **Base URL:** `https://tbg6y3.us-1.quentn.com/public/api/v1`
- **Official documentation:** [Create Email](https://help.quentn.com/hc/en-150/articles/4518209942289-Mail-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subject` | body | `string` | yes | The email subject line. |
| `body_html` | body | `string` | yes | HTML content of the email. |
| `context` | body | `string` | yes | Mail context, for example opt_in_mail or webinar_reminder. |
| `body_text` | body | `string` | no | Optional plain-text email body. |
| `sender_id` | body | `number` | no | Optional sender id from List Mail Senders. |
