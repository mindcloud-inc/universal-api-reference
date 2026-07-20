# HIPAAtizer: Native API Reference

A consolidated summary of HIPAAtizer's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://github.com/HIPAAtizer/api-docs
- **API base URL:** `https://app.hipaatizer.com`

## Authentication

### API Key

HIPAAtizer REST API authentication using an API key sent in request headers.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://raw.githubusercontent.com/HIPAAtizer/api-docs/main/README.md)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Count Future Appointments](actions/count-future-appointments.md) | `POST /api/v1/api_key/appointments/count_future` | [docs](https://github.com/HIPAAtizer/api-docs) |
| [Download Submission CSV](actions/download-submission-csv.md) | `GET /api/v1/api_key/submissions/:submissionId/csv` | [docs](https://github.com/HIPAAtizer/api-docs) |
| [Download Submission Log](actions/download-submission-log.md) | `GET /api/v1/api_key/submissions/:submissionId/logs` | [docs](https://github.com/HIPAAtizer/api-docs) |
| [Download Submission PDF](actions/download-submission-pdf.md) | `GET /api/v1/api_key/submissions/:submissionId/pdf` | [docs](https://github.com/HIPAAtizer/api-docs) |
| [Get Submission By ID](actions/get-submission-by-id.md) | `GET /api/v1/api_key/submissions/:submissionId` | [docs](https://github.com/HIPAAtizer/api-docs) |
| [List All Locations](actions/list-all-locations.md) | `GET /api/v1/api_key/locations/all` | [docs](https://github.com/HIPAAtizer/api-docs) |
| [List All Services](actions/list-all-services.md) | `GET /api/v1/api_key/services/all` | [docs](https://github.com/HIPAAtizer/api-docs) |
| [List All Workers](actions/list-all-workers.md) | `POST /api/v1/api_key/workers/all` | [docs](https://github.com/HIPAAtizer/api-docs) |
| [List New Submissions](actions/list-new-submissions.md) | `POST /api/v1/api_key/submissions/unconfirmed_list` | [docs](https://github.com/HIPAAtizer/api-docs) |
| [Search Appointments](actions/search-appointments.md) | `POST /api/v1/api_key/appointments/search` | [docs](https://github.com/HIPAAtizer/api-docs) |
| [Search Submissions](actions/search-submissions.md) | `POST /api/v1/api_key/submissions/search` | [docs](https://github.com/HIPAAtizer/api-docs) |
