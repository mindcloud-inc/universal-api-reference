# Update Campaign with Sertifier

Updates an existing campaign in Sertifier.

## Endpoint

- **Method:** `PUT`
- **Path:** `/campaign/:campaign_id`
- **Base URL:** `https://b2b.sertifier.com`
- **Official documentation:** [Update Campaign](https://sertifier.docs.apiary.io/reference/campaign/get-update-delete-campaign)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `badgeId` | body | `string` | no |
| `campaign_id` | path | `string` | yes |
| `designId` | body | `string` | no |
| `detailId` | body | `string` | no |
| `emailFromName` | body | `string` | no |
| `emailSubject` | body | `string` | no |
| `emailTemplateId` | body | `string` | no |
| `title` | body | `string` | no |
| `emailFromAddress` | body | `string` | no |
| `privateCampaign` | body | `boolean` | no |
