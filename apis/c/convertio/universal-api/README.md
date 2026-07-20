# <img src="https://images.mindcloud.co/apps/icons/convertio_1775845258071.png" alt="Convertio logo" width="28" height="28"> Convertio: Universal API

Convert files and extract OCR text with the Convertio API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/convertio/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://convertio.co
- **Vendor API docs:** https://developers.convertio.co/api/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Conversions](actions/list-conversions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convertio/latest/actions/list-conversions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Conversion

| Action | Method | Description |
| --- | --- | --- |
| [Delete Conversion](actions/delete-conversion.md) | DELETE | Deletes or cancels a conversion from Convertio. |
| [Get Conversion Status](actions/get-conversion-status.md) | GET | Retrieves a conversion status from Convertio. |
| [Get Result File Content](actions/get-result-file-content.md) | GET | Retrieves converted file content from Convertio. |
| [List Conversions](actions/list-conversions.md) | GET | Retrieves conversions and statuses from Convertio. |
| [Start Conversion](actions/start-conversion.md) | POST | Starts a conversion in Convertio. |
| [Upload Conversion File](actions/upload-conversion-file.md) | PUT | Uploads a file for a conversion in Convertio. |

