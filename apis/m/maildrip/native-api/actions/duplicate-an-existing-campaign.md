# Duplicate an existing campaign with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/campaigns/{campaignId}/duplicate`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Duplicate an existing campaign](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | ID of the campaign to duplicate |
| `newName` | body | `string` | no | Custom name for the duplicated campaign (1-100 characters). Defaults to "{originalName} (Copy)". |
