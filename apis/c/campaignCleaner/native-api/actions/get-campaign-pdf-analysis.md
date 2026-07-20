# Get Campaign PDF Analysis with Campaign Cleaner

Retrieves a campaign PDF analysis from Campaign Cleaner.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/get_campaign_pdf_analysis`
- **Base URL:** `https://api.campaigncleaner.com`
- **Official documentation:** [Get Campaign PDF Analysis](https://docs.campaigncleaner.com/api-reference/endpoint/get-campaign-pdf-analysis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign.id` | body | `string` | yes | The campaign ID to export as PDF. |
