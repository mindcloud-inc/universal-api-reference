# <img src="https://images.mindcloud.co/apps/icons/extract-monster_1775825010390.png" alt="Extract Monster logo" width="28" height="28"> Extract Monster: Universal API

AI-powered document and media extraction API for extracting structured data from files, raw bytes, and text using optional JSON schemas.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/extractMonster/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://extract.monster
- **Vendor API docs:** https://extract.monster/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/extractMonster/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Byte Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Extract Data From Bytes](actions/extract-data-from-bytes.md) | GET | Extracts structured data from file bytes in Extract Monster. |

### Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Extract Data From Text](actions/extract-data-from-text.md) | GET | Extracts structured data from text in Extract Monster. |

### File Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Extract Data From File](actions/extract-data-from-file.md) | GET | Extracts structured data from a file in Extract Monster. |

### Health

| Action | Method | Description |
| --- | --- | --- |
| [Health Check](actions/health-check.md) | GET | Retrieves health status from Extract Monster. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [Get API Info](actions/get-api-info.md) | GET | Retrieves API information from Extract Monster. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Extract Monster. |

