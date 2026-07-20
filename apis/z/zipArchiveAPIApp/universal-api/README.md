# <img src="https://images.mindcloud.co/apps/icons/zip-archive-apiapp_1773432679223.png" alt="Zip Archive API app logo" width="28" height="28"> Zip Archive API app: Universal API

Create and extract ZIP archives from files and URLs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zipArchiveAPIApp/latest
- **Category:** Content & Files / Storage
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.archiveapi.com
- **Vendor API docs:** https://archiveapi.com/rest-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Extract ZIP Archive](actions/extract-zip-archive.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zipArchiveAPIApp/latest/actions/extract-zip-archive?connectionId=$CONNECTION_ID&file=https%3A%2F%2Fgithub.com%2Fgithubtraining%2Fhellogitworld%2Farchive%2Frefs%2Fheads%2Fmaster.zip" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Archive Contents

| Action | Method | Description |
| --- | --- | --- |
| [Extract ZIP Archive](actions/extract-zip-archive.md) | GET | Extracts a ZIP archive in Zip Archive API app. |

### Zip Archive

| Action | Method | Description |
| --- | --- | --- |
| [Create ZIP Archive](actions/create-zip-archive.md) | POST | Creates a ZIP archive in Zip Archive API app. |

