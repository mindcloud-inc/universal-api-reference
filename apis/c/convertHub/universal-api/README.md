# <img src="https://images.mindcloud.co/apps/icons/convert-hub_1775760142993.png" alt="ConvertHub logo" width="28" height="28"> ConvertHub: Universal API

Convert files, check formats, and track conversion jobs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/convertHub/latest
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://converthub.com
- **Vendor API docs:** https://converthub.com/api/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Details](actions/get-account-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Details](actions/get-account-details.md) | GET | Retrieves account credits and plan details from ConvertHub. |

### Conversion Job

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Job](actions/cancel-job.md) | DELETE | Cancels an active conversion job in ConvertHub. |
| [Convert File from Base64](actions/convert-file-from-base64.md) | POST | Creates a file conversion job from base64 content in ConvertHub. |
| [Convert File from URL](actions/convert-file-from-url.md) | POST | Creates a file conversion job from a URL in ConvertHub. |
| [Delete Conversion File](actions/delete-conversion-file.md) | DELETE | Deletes a completed conversion file from ConvertHub. |
| [Get Job Status](actions/get-job-status.md) | GET | Retrieves a conversion job's status from ConvertHub. |
| [Submit File for Conversion](actions/submit-file-for-conversion.md) | POST | Creates a file conversion job in ConvertHub. |

### Conversion Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Download URL](actions/get-download-url.md) | GET | Retrieves a converted file URL or base64 content from ConvertHub. |

### Conversion Support

| Action | Method | Description |
| --- | --- | --- |
| [Check Conversion Support](actions/check-conversion-support.md) | GET | Checks whether ConvertHub supports a specific format conversion. |

### Format Catalog

| Action | Method | Description |
| --- | --- | --- |
| [Get Supported Formats](actions/get-supported-formats.md) | GET | Retrieves supported file formats from ConvertHub. |

### Format Conversion Catalog

| Action | Method | Description |
| --- | --- | --- |
| [Get Format Conversions](actions/get-format-conversions.md) | GET | Retrieves supported target formats for a source format in ConvertHub. |

### Format Conversion Map

| Action | Method | Description |
| --- | --- | --- |
| [Get All Supported Conversions](actions/get-all-supported-conversions.md) | GET | Retrieves all supported conversion mappings from ConvertHub. |

### Health

| Action | Method | Description |
| --- | --- | --- |
| [Health Check](actions/health-check.md) | GET | Retrieves API health and statistics from ConvertHub. |

### Upload Session

| Action | Method | Description |
| --- | --- | --- |
| [Complete Chunked Upload](actions/complete-chunked-upload.md) | PUT | Completes a chunked upload and starts conversion in ConvertHub. |
| [Initialize Chunked Upload](actions/initialize-chunked-upload.md) | POST | Creates a chunked upload session in ConvertHub. |
| [Upload Chunk](actions/upload-chunk.md) | PUT | Uploads one file chunk to ConvertHub. |

