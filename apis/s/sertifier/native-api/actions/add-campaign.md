# Add Campaign with Sertifier

Creates a new campaign in Sertifier.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaign`
- **Base URL:** `https://b2b.sertifier.com`
- **Official documentation:** [Add Campaign](https://sertifier.docs.apiary.io/reference/campaign/add-campaign)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `title` | body | `string` | yes |
| `detailId` | body | `string` | yes |
| `designId` | body | `string` | yes |
| `emailTemplateId` | body | `string` | yes |
| `emailFromName` | body | `string` | yes |
| `emailSubject` | body | `string` | yes |
| `emailFromAddress` | body | `string` | yes |
| `badgeId` | body | `string` | no |
| `privateCampaign` | body | `boolean` | no |
