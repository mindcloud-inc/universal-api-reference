# Update Resource Details with Cloudinary

Updates resource details in your Cloudinary account.

## Endpoint

- **Method:** `PUT`
- **Path:** `/resources/:asset_id`
- **Base URL:** `https://api.cloudinary.com/v1_1/{cloudName}`
- **Official documentation:** [Update Resource Details](https://cloudinary.com/documentation/admin_api#update_details_of_an_existing_resource_by_asset_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asset_id` | path | `string` | yes | The Cloudinary asset ID. |
| `display_name` | body | `string` | no | A user-friendly display name for the asset. |
