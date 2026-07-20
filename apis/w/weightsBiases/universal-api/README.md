# <img src="https://images.mindcloud.co/apps/icons/wab-logo_1778098132920.png" alt="Weights & Biases logo" width="28" height="28"> Weights & Biases: Universal API

Track, query, and manage W&B Weave traces, objects, tables, evaluations, feedback, and related project resources from the official Weave Service API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/weightsBiases/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://wandb.ai
- **Vendor API docs:** https://docs.wandb.ai/weave/reference/service-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Server Info](actions/get-server-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weightsBiases/latest/actions/get-server-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Alias

| Action | Method | Description |
| --- | --- | --- |
| [List Aliases](actions/list-aliases.md) | GET | Retrieves aliases from Weights & Biases. |

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Query Calls](actions/query-calls.md) | GET | Retrieves call records from Weights & Biases. |
| [Read Call](actions/read-call.md) | GET | Retrieves a call record from Weights & Biases. |

### Call Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Calls Count](actions/get-calls-count.md) | GET | Retrieves call counts from Weights & Biases. |

### Call Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Call Stats](actions/get-call-stats.md) | GET | Retrieves call statistics from Weights & Biases. |

### Call Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Calls Usage](actions/get-calls-usage.md) | GET | Retrieves call usage metrics from Weights & Biases. |

### Caller Location

| Action | Method | Description |
| --- | --- | --- |
| [Get Caller Location](actions/get-caller-location.md) | GET | Retrieves caller location details from Weights & Biases. |

### Cost

| Action | Method | Description |
| --- | --- | --- |
| [Query Costs](actions/query-costs.md) | GET | Retrieves cost records from Weights & Biases. |

### Feedback

| Action | Method | Description |
| --- | --- | --- |
| [Query Feedback](actions/query-feedback.md) | GET | Retrieves feedback records from Weights & Biases. |

### Feedback Payload Schema

| Action | Method | Description |
| --- | --- | --- |
| [Get Feedback Payload Schema](actions/get-feedback-payload-schema.md) | GET | Retrieves feedback payload schema from Weights & Biases. |

### Feedback Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Feedback Stats](actions/get-feedback-stats.md) | GET | Retrieves feedback statistics from Weights & Biases. |

### File Content

| Action | Method | Description |
| --- | --- | --- |
| [Get File Content](actions/get-file-content.md) | GET | Retrieves file content from Weights & Biases. |

### Files Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Files Stats](actions/get-files-stats.md) | GET | Retrieves file storage statistics from Weights & Biases. |

### Health Status

| Action | Method | Description |
| --- | --- | --- |
| [Read Root](actions/read-root.md) | GET | Retrieves root health status from Weights & Biases. |

### Object

| Action | Method | Description |
| --- | --- | --- |
| [Query Objects](actions/query-objects.md) | GET | Retrieves object versions from Weights & Biases. |
| [Read Object](actions/read-object.md) | GET | Retrieves an object version from Weights & Biases. |

### Project Info

| Action | Method | Description |
| --- | --- | --- |
| [Get Projects Info](actions/get-projects-info.md) | GET | Retrieves project identifiers from Weights & Biases. |

### Reference

| Action | Method | Description |
| --- | --- | --- |
| [Read Refs Batch](actions/read-refs-batch.md) | GET | Retrieves refs in batch from Weights & Biases. |

### Server Info

| Action | Method | Description |
| --- | --- | --- |
| [Get Server Info](actions/get-server-info.md) | GET | Retrieves trace server information from Weights & Biases. |

### Table Row

| Action | Method | Description |
| --- | --- | --- |
| [Query Table](actions/query-table.md) | GET | Retrieves table rows from Weights & Biases. |

### Table Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Table Stats](actions/get-table-stats.md) | GET | Retrieves table statistics from Weights & Biases. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from Weights & Biases. |

### Thread

| Action | Method | Description |
| --- | --- | --- |
| [Query Threads](actions/query-threads.md) | GET | Retrieves threads from Weights & Biases. |

### Version

| Action | Method | Description |
| --- | --- | --- |
| [Read Version](actions/read-version.md) | GET | Retrieves the trace service version from Weights & Biases. |

