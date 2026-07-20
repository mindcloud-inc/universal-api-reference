# Send Email Campaign Test with Brevo

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/emailCampaigns/:campaignId/sendTest`
- **Base URL:** `https://api.brevo.com`
- **Official documentation:** [Send Email Campaign Test](https://developers.brevo.com/reference/sendtestemailtocampaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `number` | yes | The email campaign identifier. |
| `emailTo[]` | body | `array<string>` | yes | Recipient email addresses for the test send. Send multiple values as a array. |
