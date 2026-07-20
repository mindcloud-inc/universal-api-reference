# Send Transactional Email with BlueFox Email

Sends a transactional email through BlueFox Email.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/send-transactional`
- **Base URL:** `https://api.bluefox.email`
- **Official documentation:** [Send Transactional Email](https://bluefox.email/docs/api/send-transactional-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string<string>` | yes | Recipient email address for the transactional email. |
| `transactionalId` | body | `string` | yes | BlueFox transactional email ID. |
