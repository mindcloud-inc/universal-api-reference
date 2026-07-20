# Poll webhook event with LeadTable

## Endpoint

- **Method:** `GET`
- **Path:** `/pollWebhook/{campaignID}/{topic}`
- **Base URL:** `https://api.lead-table.com/api/v3/external`
- **Official documentation:** [Poll webhook event](https://docs.lead-table.com/leadtable-external-api-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignID` | path | `string` | yes | The campaign or table used for the webhook sample event. |
| `topic` | path | `list` | yes | Webhook topic to poll. Accepted values: `Change status`, `Delete lead`, `New lead`, `New table`, `Update lead`. |
