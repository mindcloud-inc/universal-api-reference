# Add Prospects in Bulk with ManyReach

Creates prospects in bulk in ManyReach.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.manyreach.com/api/v2/prospects/bulk`
- **Base URL:** `https://api.manyreach.com`
- **Official documentation:** [Add Prospects in Bulk](https://api.manyreach.com/api#v2/tag/prospect)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | query | `string` | yes | Required list ID to which all prospects will be added |
| `campaignId` | query | `string` | no | Optional campaign ID to add prospects to |
| `addOnlyIfNew` | query | `boolean` | no | Only add prospects that are new in CRM |
| `notInOtherCampaign` | query | `boolean` | no | Check if prospect is already in other campaigns |
| `prospects` | body | `list<object>` | yes | Array of prospect objects to create in bulk. |
