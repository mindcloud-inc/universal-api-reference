# <img src="https://images.mindcloud.co/apps/icons/eye-levelai_1775769371805.png" alt="EyeLevel.ai logo" width="28" height="28"> EyeLevel.ai: Universal API

Ingest documents, search knowledge, and build RAG applications

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eyeLevelai/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.eyelevel.ai/
- **Vendor API docs:** https://docs.eyelevel.ai/documentation/fundamentals/welcome

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Customer](actions/get-customer.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eyeLevelai/latest/actions/get-customer?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET | Retrieves account information from EyeLevel.ai. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Crawl Website](actions/crawl-website.md) | POST | Crawls a website into EyeLevel.ai for ingestion. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from EyeLevel.ai. |
| [Lookup Documents](actions/lookup-documents.md) | GET | Retrieves documents in EyeLevel.ai by process, bucket, or group. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Bucket](actions/create-bucket.md) | POST | Creates a new bucket in EyeLevel.ai. |
| [Delete Bucket](actions/delete-bucket.md) | DELETE | Deletes an existing bucket from EyeLevel.ai. |
| [Get Bucket](actions/get-bucket.md) | GET | Retrieves a bucket from EyeLevel.ai. |
| [List Buckets](actions/list-buckets.md) | GET | Retrieves buckets from EyeLevel.ai. |
| [Update Bucket](actions/update-bucket.md) | PUT | Updates an existing bucket in EyeLevel.ai. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Add Bucket To Group](actions/add-bucket-to-group.md) | POST | Adds a bucket to a group in EyeLevel.ai. |
| [Create Group](actions/create-group.md) | POST | Creates a new group in EyeLevel.ai. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from EyeLevel.ai. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from EyeLevel.ai. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from EyeLevel.ai. |
| [Remove Bucket From Group](actions/remove-bucket-from-group.md) | DELETE | Removes a bucket from a group in EyeLevel.ai. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in EyeLevel.ai. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Health Status](actions/get-health-status.md) | GET | Retrieves a service health status from EyeLevel.ai. |
| [Get Processing Status](actions/get-processing-status.md) | GET | Retrieves an ingest process status from EyeLevel.ai. |
| [List Health Statuses](actions/list-health-statuses.md) | GET | Retrieves health statuses from EyeLevel.ai. |
| [List Ingest Processes](actions/list-ingest-processes.md) | GET | Retrieves ingest processes from EyeLevel.ai. |

