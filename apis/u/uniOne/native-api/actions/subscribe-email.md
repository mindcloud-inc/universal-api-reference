# Subscribe Email with UniOne

Subscribes an email address through UniOne.

## Endpoint

- **Method:** `POST`
- **Path:** `email/subscribe.json`
- **Base URL:** `https://api.unione.io/en/transactional/api/v1`
- **Official documentation:** [Subscribe Email](https://docs.unione.io/en/web-api-ref#email-subscribe)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_email` | body | `string` | yes | Sender email address. |
| `from_name` | body | `string` | yes | Sender name. |
| `to_email` | body | `string` | yes | Recipient email address. |
