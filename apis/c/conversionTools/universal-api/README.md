# <img src="https://images.mindcloud.co/apps/icons/conversion-tools_1773956200361.png" alt="Conversion Tools logo" width="28" height="28"> Conversion Tools: Universal API

Convert files, documents, media, and structured data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/conversionTools/latest
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://conversiontools.io
- **Vendor API docs:** https://conversiontools.io/api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authenticated User Info](actions/get-authenticated-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conversionTools/latest/actions/get-authenticated-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Download File](actions/download-file.md) | GET | Downloads a file from Conversion Tools. |
| [Get File Metadata](actions/get-file-metadata.md) | GET | Retrieves file metadata from Conversion Tools. |
| [Upload File](actions/upload-file.md) | POST | Uploads a new file to Conversion Tools. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Conversion Task](actions/create-conversion-task.md) | POST | Creates a new conversion task in Conversion Tools. |
| [Delete Task Files Immediately](actions/delete-task-files-immediately.md) | DELETE | Permanently deletes a task's files from Conversion Tools. |
| [Get Task Status](actions/get-task-status.md) | GET | Retrieves the current status of a conversion task from Conversion Tools. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves up to 50 recent conversion tasks from Conversion Tools. |
| [Update Task Retention](actions/update-task-retention.md) | PUT | Updates an existing task retention mode in Conversion Tools. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get API Configuration](actions/get-api-configuration.md) | GET | Retrieves available conversion types and options from Conversion Tools. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Authenticated User Info](actions/get-authenticated-user-info.md) | GET | Retrieves authenticated user info from Conversion Tools. |

