# Create Transactional Campaign with Sender

## Endpoint

- **Method:** `POST`
- **Path:** `/transactional`
- **Base URL:** `https://api.sender.net/v2`
- **Official documentation:** [Create Transactional Campaign](https://api.sender.net/transactional_campaigns/create/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | no | Name of the campaign shown in reports. |
| `subject` | body | `string` | yes | Subject line of the campaign. |
| `from` | body | `string` | yes | Sender name displayed to recipients. |
| `reply_to` | body | `string` | yes | Sender email. Must belong to a verified domain. |
| `editor` | body | `string` | yes | One of plain, html, or builder. |
| `preheader` | body | `string` | no | Preview text of the email. |
| `content` | body | `string` | no | Campaign content for plain or html transactional emails. |
