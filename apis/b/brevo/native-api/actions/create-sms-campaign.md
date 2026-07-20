# Create SMS Campaign with Brevo

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/smsCampaigns`
- **Base URL:** `https://api.brevo.com`
- **Official documentation:** [Create SMS Campaign](https://developers.brevo.com/reference/createsmscampaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | The SMS message content. |
| `name` | body | `string` | yes | The SMS campaign name. |
| `sender` | body | `string` | yes | The sender name for the SMS campaign. |
