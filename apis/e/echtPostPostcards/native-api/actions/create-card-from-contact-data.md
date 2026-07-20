# Create Card From Contact Data with EchtPost Postcards

Creates a postcard from contact data in EchtPost Postcards.

## Endpoint

- **Method:** `POST`
- **Path:** `/cards`
- **Base URL:** `https://api.echtpost.de/v1`
- **Official documentation:** [Create Card From Contact Data](https://hilfe.echtpost.de/article/453/postkartenversand-uber-api-programmierschnittstelle)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `city` | body | `string` | yes | Recipient city. |
| `company_name` | body | `string` | no | Recipient company name. |
| `content_vertical` | body | `string` | no | Optional vertical text printed on the card edge. |
| `country_code` | body | `string` | yes | Recipient country code. |
| `deliver_at` | body | `date` | yes | The mailing date (YYYY-MM-DD). |
| `first` | body | `string` | yes | Recipient first name. |
| `name` | body | `string` | yes | Recipient last name. |
| `notification_date` | body | `date` | no | Optional notification date (YYYY-MM-DD). |
| `notification_email` | body | `string` | no | Optional notification recipient email. |
| `notification_type` | body | `list` | no | Optional email timing. Accepted values: `0`, `1`. |
| `sandbox` | query | `list` | no | Set to 1 to validate without creating a postcard. Accepted values: `0`, `1`. |
| `state_code` | body | `string` | no | Recipient state code. |
| `street` | body | `string` | yes | Recipient street. |
| `templateId` | body | `number` | yes | The template to send. |
| `title` | body | `string` | no | Recipient title. |
| `zip` | body | `string` | yes | Recipient zip code. |
