# Update Campaign with Sendloop

## Endpoint

- **Method:** `POST`
- **Path:** `/campaign.update/json`
- **Base URL:** `https://{subdomain}.sendloop.com/api/v3`
- **Official documentation:** [Update Campaign](https://chmyos.notion.site/Update-details-of-a-Campaign-89e59c4024244874944093c47fb61039)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CampaignID` | body | `number` | yes | ID number of the target campaign |
| `CampaignName` | body | `string` | no | Name of your campaign |
| `FromName` | body | `string` | no | The name shown in the from email header |
| `FromEmail` | body | `string` | no | Sender email address |
| `ReplyToName` | body | `string` | no | The name shown in the reply-to header |
| `ReplyToEmail` | body | `string` | no | Email address to receive replies |
| `TargetListIDs` | body | `string` | no | ID numbers of recipient lists |
| `Subject` | body | `string` | no | Subject of your email campaign |
