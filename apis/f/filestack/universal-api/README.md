# <img src="https://images.mindcloud.co/apps/icons/filestack-icon-filled-256_1774648920509.png" alt="Filestack logo" width="28" height="28"> Filestack: Universal API

Filestack File API integration for uploading, retrieving metadata for, overwriting, downloading, and deleting files via Filestack handles.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/filestack/latest
- **Category:** Content & Files / Storage
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.filestack.com
- **Vendor API docs:** https://www.filestack.com/docs/api/file/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get File Metadata](actions/get-file-metadata.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filestack/latest/actions/get-file-metadata?connectionId=$CONNECTION_ID&handle=DCL5K46FS3OIxb5iuKby" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### File

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE | Deletes an existing file from Filestack. |
| [Get File Metadata](actions/get-file-metadata.md) | GET | Retrieves file metadata from Filestack. |
| [Store File From URL](actions/store-file-from-url.md) | POST | Creates a new file in Filestack from a URL. |

### Workflow Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow Status](actions/get-workflow-status.md) | GET | Retrieves workflow status from Filestack. |
| [Run Workflow On File](actions/run-workflow-on-file.md) | POST | Runs a workflow on a file in Filestack. |

