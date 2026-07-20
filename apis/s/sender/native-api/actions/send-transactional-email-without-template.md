# Send Transactional Email Without Template with Sender

## Endpoint

- **Method:** `POST`
- **Path:** `/message/send`
- **Base URL:** `https://api.sender.net/v2`
- **Official documentation:** [Send Transactional Email Without Template](https://api.sender.net/transactional_campaigns/send-transactional/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `object` | yes | Sender object containing email and name. |
| `to` | body | `object` | yes | Recipient object containing required email and optional name. |
| `subject` | body | `string` | yes | Subject line of the email. |
| `text` | body | `string` | no | Plain-text version of the email body. |
| `html` | body | `string` | no | HTML version of the email body. |
| `headers` | body | `object` | no | Optional headers to include. |
| `variables` | body | `object` | no | Key-value variables for personalization. |
| `attachments` | body | `object` | no | Filename-to-URL attachment map. |
