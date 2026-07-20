# Apply Campaign with Karma CRM

Applies a campaign to a record in Karma CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/campaign_entries/apply`
- **Base URL:** `https://app.karmacrm.com`
- **Official documentation:** [Apply Campaign](https://docs.karmacrm.com/#apply-campaign-create-a-campaign-entries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_entry` | body | `object` | yes | Campaign-entry payload object containing record_id, record_type, and campaign_id. |
