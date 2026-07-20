# Create Card From Contact List with EchtPost Postcards

Creates postcards for a contact list in EchtPost Postcards.

## Endpoint

- **Method:** `POST`
- **Path:** `/cards`
- **Base URL:** `https://api.echtpost.de/v1`
- **Official documentation:** [Create Card From Contact List](https://hilfe.echtpost.de/article/453/postkartenversand-uber-api-programmierschnittstelle)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_ids` | body | `string` | yes | Comma-separated EchtPost contact IDs. |
| `content_vertical` | body | `string` | no | Optional vertical text printed on the card edge. |
| `deliver_at` | body | `date` | yes | The mailing date (YYYY-MM-DD). |
| `notification_date` | body | `date` | no | Optional notification date (YYYY-MM-DD). |
| `notification_email` | body | `string` | no | Optional notification recipient email. |
| `notification_type` | body | `list` | no | Optional email timing. Accepted values: `0`, `1`. |
| `sandbox` | query | `list` | no | Set to 1 to validate without creating a postcard. Accepted values: `0`, `1`. |
| `templateId` | body | `number` | yes | The template to send. |
