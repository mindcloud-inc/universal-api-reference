# Create Email Campaign with Brevo

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/emailCampaigns`
- **Base URL:** `https://api.brevo.com`
- **Official documentation:** [Create Email Campaign](https://developers.brevo.com/reference/create-email-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `htmlContent` | body | `string` | yes | HTML content of the email. |
| `name` | body | `string` | yes | Email campaign name. |
| `recipients` | body | `object` | yes | Recipients object containing list IDs or segment IDs. |
| `sender` | body | `object` | yes | Sender object with name and email. |
| `subject` | body | `string` | yes | Email campaign subject line. |
| `type` | body | `string` | no | Campaign type, for example classic. |
