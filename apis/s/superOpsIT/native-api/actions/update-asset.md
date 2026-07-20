# Update Asset with SuperOps IT

## Endpoint

- **Method:** `POST`
- **Path:** `/it`
- **Base URL:** `https://api.superops.ai`
- **Official documentation:** [Update Asset](https://developer.superops.com/it#mutation-updateAsset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assetId` | body | `string` | yes | The SuperOps asset ID to update. |
| `name` | body | `string` | no | Optional new asset name. |
| `siteId` | body | `string` | no | Optional site ID for the asset. |
| `requesterUserId` | body | `string` | no | Optional requester user ID. |
| `purchasedDate` | body | `date` | no | Optional purchased date in YYYY-MM-DD format. |
| `warrantyExpiryDate` | body | `date` | no | Optional warranty expiry date in YYYY-MM-DD format. |
