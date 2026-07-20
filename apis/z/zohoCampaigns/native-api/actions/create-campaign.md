# Create Campaign with Zoho Campaigns

Creates a campaign in Zoho Campaigns.

## Endpoint

- **Method:** `POST`
- **Path:** `/createCampaign`
- **Base URL:** `https://campaigns.zoho.com/api/v1.1`
- **Official documentation:** [Create Campaign](https://www.zoho.com/campaigns/help/developers/create-campaign.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignname` | query | `string` | yes | Name for the campaign. |
| `from_email` | query | `string` | yes | Verified sender email address for the campaign. |
| `subject` | query | `string` | yes | Subject line for the campaign. |
| `content_url` | query | `string` | no | Public HTML URL used as the campaign content source. |
| `list_details` | query | `string` | yes | List-to-segment mapping in Zoho's documented string format. |
| `topicId` | query | `list<string>` | no | Topic ID required on accounts that use Zoho's updated topic management. |
