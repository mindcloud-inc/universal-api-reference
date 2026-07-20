# <img src="https://images.mindcloud.co/apps/icons/hipaatizer-icon-filled-256_1775079166574.png" alt="HIPAAtizer logo" width="28" height="28"> HIPAAtizer: Universal API

HIPAAtizer API for HIPAA-compliant forms, submissions, appointments, and related operations for healthcare workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hIPAAtizer/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.hipaatizer.com
- **Vendor API docs:** https://github.com/HIPAAtizer/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List All Locations](actions/list-all-locations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hIPAAtizer/latest/actions/list-all-locations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Appointments

| Action | Method | Description |
| --- | --- | --- |
| [Count Future Appointments](actions/count-future-appointments.md) | GET | Retrieves the count of future appointments in HIPAAtizer. |
| [Search Appointments](actions/search-appointments.md) | GET | Finds appointments in HIPAAtizer by location, service, or date. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [List All Locations](actions/list-all-locations.md) | GET | Retrieves all account locations from HIPAAtizer. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [List All Services](actions/list-all-services.md) | GET | Retrieves all available services from HIPAAtizer. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Download Submission CSV](actions/download-submission-csv.md) | GET | Retrieves submission data as CSV from HIPAAtizer. |
| [Download Submission Log](actions/download-submission-log.md) | GET | Retrieves submission access logs from HIPAAtizer. |
| [Download Submission PDF](actions/download-submission-pdf.md) | GET | Retrieves a submission PDF from HIPAAtizer. |
| [Get Submission By ID](actions/get-submission-by-id.md) | GET | Retrieves a submission by ID from HIPAAtizer. |
| [List All Workers](actions/list-all-workers.md) | GET | Retrieves workers from HIPAAtizer for selected locations. |
| [List New Submissions](actions/list-new-submissions.md) | GET | Retrieves new submissions from HIPAAtizer by workflow or location. |
| [Search Submissions](actions/search-submissions.md) | GET | Finds submissions in HIPAAtizer by workflow and search criteria. |

