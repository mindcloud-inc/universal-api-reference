# Cloudinary: Native API Reference

A consolidated summary of Cloudinary's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://cloudinary.com/documentation/cloudinary_references
- **API base URL:** `https://api.cloudinary.com/v1_1/{cloudName}`

## Authentication

### Basic Auth

Use your Cloudinary API key and API secret with your cloud name.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Cloud Name:** `cloudName` · required · Your Cloudinary cloud name.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://cloudinary.com/documentation/image_upload_api_reference#authentication_methods)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `max_results` in the query string to set the page size (maximum 500). Use `next_cursor` in the query string as the pagination cursor.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Apply Explicit Asset Actions](actions/apply-explicit-asset-actions.md) | `POST /:resource_type/explicit` | [docs](https://cloudinary.com/documentation/image_upload_api_reference#explicit_method) |
| [Create Folder](actions/create-folder.md) | `POST /folders/:folder` | [docs](https://cloudinary.com/documentation/admin_api#folders) |
| [Create Upload Preset](actions/create-upload-preset.md) | `POST /upload_presets` | [docs](https://cloudinary.com/documentation/admin_api#upload_presets) |
| [Delete Asset](actions/delete-asset.md) | `POST /:resource_type/destroy` | [docs](https://cloudinary.com/documentation/image_upload_api_reference#destroy_method) |
| [Delete Folder](actions/delete-folder.md) | `DELETE /folders/:folder` | [docs](https://cloudinary.com/documentation/admin_api#delete_folder) |
| [Delete Resources by Asset IDs](actions/delete-resources-by-asset-ids.md) | `DELETE /resources` | [docs](https://cloudinary.com/documentation/admin_api#delete_resources) |
| [Delete Resources by Public IDs](actions/delete-resources-by-public-ids.md) | `DELETE /resources/:resource_type/:type` | [docs](https://cloudinary.com/documentation/admin_api#delete_resources) |
| [Delete Upload Preset](actions/delete-upload-preset.md) | `DELETE /upload_presets/:name` | [docs](https://cloudinary.com/documentation/admin_api#delete_an_upload_preset) |
| [Get Resource by Asset ID](actions/get-resource-by-asset-id.md) | `GET /resources/:asset_id` | [docs](https://cloudinary.com/documentation/admin_api#details_of_a_single_resource_by_asset_id) |
| [Get Resource by Public ID](actions/get-resource-by-public-id.md) | `GET /resources/:resource_type/:type/:public_id` | [docs](https://cloudinary.com/documentation/admin_api#details_of_a_single_resource_by_public_id) |
| [Get Upload Preset](actions/get-upload-preset.md) | `GET /upload_presets/:name` | [docs](https://cloudinary.com/documentation/admin_api#upload_presets) |
| [Get Usage](actions/get-usage.md) | `GET /usage` | [docs](https://cloudinary.com/documentation/admin_api#usage) |
| [List Folders](actions/list-folders.md) | `GET /folders` | [docs](https://cloudinary.com/documentation/admin_api#folders) |
| [List Resources](actions/list-resources.md) | `GET /resources/:resource_type/:type` | [docs](https://cloudinary.com/documentation/admin_api#resources) |
| [List Resources by Asset Folder](actions/list-resources-by-asset-folder.md) | `GET /resources/by_asset_folder` | [docs](https://cloudinary.com/documentation/admin_api#resources_by_asset_folder) |
| [List Resources by Tag](actions/list-resources-by-tag.md) | `GET /resources/:resource_type/tags/:tag` | [docs](https://cloudinary.com/documentation/admin_api#resources_by_tag) |
| [List Subfolders](actions/list-subfolders.md) | `GET /folders/:folder` | [docs](https://cloudinary.com/documentation/admin_api#folders) |
| [List Tags](actions/list-tags.md) | `GET /tags/:resource_type` | [docs](https://cloudinary.com/documentation/admin_api#tags) |
| [List Upload Presets](actions/list-upload-presets.md) | `GET /upload_presets` | [docs](https://cloudinary.com/documentation/admin_api#upload_presets) |
| [Ping](actions/ping.md) | `GET /ping` | [docs](https://cloudinary.com/documentation/admin_api#ping) |
| [Rename Asset](actions/rename-asset.md) | `POST /:resource_type/rename` | [docs](https://cloudinary.com/documentation/image_upload_api_reference#rename_method) |
| [Search Folders](actions/search-folders.md) | `GET /folders/search` | [docs](https://cloudinary.com/documentation/admin_api#search_folders) |
| [Search Resources](actions/search-resources.md) | `GET /resources/search` | [docs](https://cloudinary.com/documentation/admin_api#search) |
| [Update Resource Details](actions/update-resource-details.md) | `PUT /resources/:asset_id` | [docs](https://cloudinary.com/documentation/admin_api#update_details_of_an_existing_resource_by_asset_id) |
| [Update Upload Preset](actions/update-upload-preset.md) | `PUT /upload_presets/:name` | [docs](https://cloudinary.com/documentation/admin_api#upload_presets) |
| [Upload Asset](actions/upload-asset.md) | `POST /:resource_type/upload` | [docs](https://cloudinary.com/documentation/image_upload_api_reference#upload_method) |
