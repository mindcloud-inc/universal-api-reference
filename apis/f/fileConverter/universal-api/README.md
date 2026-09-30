# <img src="https://images.mindcloud.co/apps/icons/file-converter-icon_1782393402002.png" alt="File Converter logo" width="28" height="28"> File Converter: Universal API

Convert files to Base64, Binary, or raw string.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fileConverter/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Convert File](actions/convert-file.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fileConverter/latest/actions/convert-file?connectionId=$CONNECTION_ID&file=string&outputFormat=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Convert File](actions/convert-file.md) | GET | Convert a file to a specific format |

