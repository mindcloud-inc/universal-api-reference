# WellTraq: Native API Reference

A consolidated summary of WellTraq's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://www.welltraq.com/api/v1
- **API base URL:** `https://welltraq.com/api/v1`

## Authentication

### Basic Auth

Authenticate WellTraq API requests with the provider-documented Basic auth username and password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://www.welltraq.com/api/v1/Endpoints/Examples)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get All Asset Form Types For Asset](actions/get-all-asset-form-types-for-asset.md) | `GET /AssetFormTypes/GetAllForAsset` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-AssetFormTypes-GetAllForAsset_assetId) |
| [Get All Asset Measurement Types For Asset](actions/get-all-asset-measurement-types-for-asset.md) | `GET /AssetMeasurementTypes/GetAllForAsset` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-AssetMeasurementTypes-GetAllForAsset_assetId) |
| [Get Asset](actions/get-asset.md) | `GET /Assets` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-Assets_assetId_includeAllAncestors) |
| [Get Asset Form Type](actions/get-asset-form-type.md) | `GET /AssetFormTypes` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-AssetFormTypes_assetFormTypeId) |
| [Get Asset Group](actions/get-asset-group.md) | `GET /AssetGroups` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-AssetGroups_assetGroupId) |
| [Get Asset Measurement Type](actions/get-asset-measurement-type.md) | `GET /AssetMeasurementTypes` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-AssetMeasurementTypes_assetMeasurementTypeId) |
| [Get Asset Type](actions/get-asset-type.md) | `GET /AssetTypes` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-AssetTypes_assetTypeId) |
| [Get Attachment](actions/get-attachment.md) | `GET /Attachments` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-Attachments_attachmentId) |
| [Get Attachment Category](actions/get-attachment-category.md) | `GET /AttachmentCategories` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-AttachmentCategories_attachmentCategoryId) |
| [Get Attachment Content](actions/get-attachment-content.md) | `GET /Attachments/GetContent` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-Attachments-GetContent_attachmentId_startIndex_chunkSize) |
| [Get Attachment File](actions/get-attachment-file.md) | `GET /Attachments/GetFile` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-Attachments-GetFile_attachmentId_openInBrowser) |
| [Get Data Type](actions/get-data-type.md) | `GET /DataTypes` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-DataTypes_dataTypeId) |
| [Get Form Analytics Fields](actions/get-form-analytics-fields.md) | `GET /Forms/GetAnalyticsFields` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-Forms-GetAnalyticsFields_formTypeName_formTypeFieldNameText_beginDate_endDate) |
| [Get Form Content](actions/get-form-content.md) | `GET /Forms/GetContent` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-Forms-GetContent_formFieldValueId_startIndex_chunkSize) |
| [Get Form File](actions/get-form-file.md) | `GET /Forms/GetFile` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-Forms-GetFile_formFieldValueId_maxWidth_maxHeight_openInBrowser) |
| [List Asset Form Types](actions/list-asset-form-types.md) | `GET /AssetFormTypes` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-AssetFormTypes_assetId_formTypeId) |
| [List Asset Groups](actions/list-asset-groups.md) | `GET /AssetGroups` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-AssetGroups_parentGroupId_take_skip_sort[0]-Field_sort[0]-Dir_sort[1]-Field_sort[1]-Dir) |
| [List Asset Groups By Last Modified Date](actions/list-asset-groups-by-last-modified-date.md) | `GET /AssetGroups/ByLastModifiedDate` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-AssetGroups-ByLastModifiedDate_beginDate_endDate) |
| [List Asset Measurement Types](actions/list-asset-measurement-types.md) | `GET /AssetMeasurementTypes` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-AssetMeasurementTypes_assetId_measurementTypeId) |
| [List Asset Types](actions/list-asset-types.md) | `GET /AssetTypes` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-AssetTypes_take_skip_sort[0]-Field_sort[0]-Dir_sort[1]-Field_sort[1]-Dir) |
| [List Assets](actions/list-assets.md) | `GET /Assets` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-Assets_assetTypeId_assetGroupId_parentAssetId_take_skip_sort[0]-Field_sort[0]-Dir_sort[1]-Field_sort[1]-Dir) |
| [List Assets By Last Modified Date](actions/list-assets-by-last-modified-date.md) | `GET /Assets/ByLastModifiedDate` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-Assets-ByLastModifiedDate_assetTypeId_beginDate_endDate) |
| [List Attachment Categories](actions/list-attachment-categories.md) | `GET /AttachmentCategories` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-AttachmentCategories_take_skip_sort[0]-Field_sort[0]-Dir_sort[1]-Field_sort[1]-Dir) |
| [List Attachments](actions/list-attachments.md) | `GET /Attachments` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-Attachments_assetId_includeContent_take_skip_sort[0]-Field_sort[0]-Dir_sort[1]-Field_sort[1]-Dir) |
| [List Attachments By Last Modified Date](actions/list-attachments-by-last-modified-date.md) | `GET /Attachments/ByLastModifiedDate` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-Attachments-ByLastModifiedDate_assetId_beginDate_endDate_includeContent) |
| [List Attachments By Upload Date](actions/list-attachments-by-upload-date.md) | `GET /Attachments/ByUploadDate` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-Attachments-ByUploadDate_assetId_beginDate_endDate_includeContent) |
| [List Audit Log](actions/list-audit-log.md) | `GET /AuditLog` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-AuditLog_tables_startDateTime_endDateTime_skip_take) |
| [List Data Types](actions/list-data-types.md) | `GET /DataTypes` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-DataTypes) |
| [List Forms By Effective Date](actions/list-forms-by-effective-date.md) | `GET /Forms/ByEffectiveDate` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-Forms-ByEffectiveDate_assetId_formTypeId_beginDate_endDate_includeAttachmentContent) |
| [List Forms By Last Modified Date](actions/list-forms-by-last-modified-date.md) | `GET /Forms/ByLastModifiedDate` | [docs](https://www.welltraq.com/api/v1/Endpoints/Api/GET-Forms-ByLastModifiedDate_assetId_formTypeId_beginDate_endDate_includeAttachmentContent) |
