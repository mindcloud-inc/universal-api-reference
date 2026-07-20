# <img src="https://images.mindcloud.co/apps/icons/fileio_1777545132763.png" alt="File.io logo" width="28" height="28"> File.io: Universal API

Share, manage, and retrieve temporary files through File.io's public REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fileio/latest
- **Category:** Content & Files / Storage
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.file.io/
- **Vendor API docs:** https://www.file.io/developers

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Files](actions/list-files.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fileio/latest/actions/list-files?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### File

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE | Deletes a file from File.io by key. |
| [Download File](actions/download-file.md) | GET | Downloads a file from File.io by key. |
| [List Files](actions/list-files.md) | GET | Retrieves files from File.io. |
| [Replace File](actions/replace-file.md) | PUT | Updates a file in File.io, resetting omitted fields. |
| [Update File](actions/update-file.md) | PUT | Updates a file in File.io, retaining omitted fields. |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to File.io. |

