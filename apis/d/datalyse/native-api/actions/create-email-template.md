# Create Email Template with Datalyse

Creates a new email template in Datalyse.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/emails/templates/create.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Create Email Template](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html` | body | `string` | yes | Template HTML content |
| `name` | body | `string` | yes | Template name |
| `subject` | body | `string` | no | Default email subject (optional) |
