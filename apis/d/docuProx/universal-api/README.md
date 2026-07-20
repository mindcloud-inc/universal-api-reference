# <img src="https://images.mindcloud.co/apps/icons/docu-prox_1774899881444.png" alt="DocuProx logo" width="28" height="28"> DocuProx: Universal API

Extract document data, submit jobs, and retrieve results

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/docuProx/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://docuprox.com
- **Vendor API docs:** https://docuprox.com/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Job Status](actions/get-job-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuProx/latest/actions/get-job-status?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Process Document](actions/process-document.md) | POST |  |
| [Process Document Binary Upload](actions/process-document-binary-upload.md) | POST |  |
| [Process Document with Agent](actions/process-document-with-agent.md) | POST |  |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Processing Job](actions/create-processing-job.md) | POST |  |
| [Get Job Status](actions/get-job-status.md) | GET |  |
| [Retrieve Job Results](actions/retrieve-job-results.md) | GET |  |

