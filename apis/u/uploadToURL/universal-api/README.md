# <img src="https://images.mindcloud.co/apps/icons/upload-to-url_1775075005939.png" alt="Upload to URL logo" width="28" height="28"> Upload to URL: Universal API

Upload, host, and manage files with instant public CDN URLs via Upload to URL's REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/uploadToURL/latest
- **Category:** Content & Files / Storage
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://uploadtourl.com
- **Vendor API docs:** https://uploadtourl.com/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get File Information](actions/get-file-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uploadToURL/latest/actions/get-file-information?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### File

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE |  |
| [Get File Information](actions/get-file-information.md) | GET |  |
| [Upload File](actions/upload-file.md) | POST |  |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Publish HTML](actions/publish-html.md) | POST |  |

