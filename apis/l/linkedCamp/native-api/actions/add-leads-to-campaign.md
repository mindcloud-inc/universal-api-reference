# Add Leads To Campaign with LinkedCamp

## Endpoint

- **Method:** `POST`
- **Path:** `/leads/add-to-campaign`
- **Base URL:** `https://api.linkedcamp.com`
- **Official documentation:** [Add Leads To Campaign](https://api.linkedcamp.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | body | `string` | yes | Campaign identifier. |
| `leads[]` | body | `array<object>` | yes | Array of leads to add to the campaign. |
