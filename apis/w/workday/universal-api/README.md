# <img src="https://images.mindcloud.co/apps/icons/favicon-www-workday-com-48x48_1782311713391.png" alt="Workday logo" width="28" height="28"> Workday: Universal API

Workday scaffold based on the attached Time Tracking v5 OpenAPI spec. Current scope covers worker retrieval plus worker time block retrieval and create/update shells for timesheet-style entries.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/workday/latest
- **Category:** Human Resources / HRIS
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.workday.com
- **Vendor API docs:** https://community.workday.com/sites/default/files/file-hosting/restapi/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Workers](actions/get-workers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workday/latest/actions/get-workers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Get Token](actions/get-token.md) | GET | Exchange a refresh token for a new Workday access token. |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Profiles](actions/get-job-profiles.md) | GET |  |
| [Get Person](actions/get-person.md) | GET | Get a single person from the Workday Person API by Workday person ID. |
| [Get Worker](actions/get-worker.md) | GET | Get a single worker from Workday Time Tracking by Workday worker ID. |
| [Get Workers](actions/get-workers.md) | GET | List workers from Workday Time Tracking with optional name or worker ID search, visibility filtering, and pagination. |
| [Get Workers History](actions/get-workers-history.md) | GET |  |
| [List People](actions/list-people.md) | GET | List people from the Workday Person API, optionally filtering by universal ID. |
| [List Time Tracking Workers](actions/list-time-tracking-workers.md) | GET | List workers from Workday Time Tracking with optional search, organization visibility filtering, and pagination. |
| [List Worker Organizations](actions/list-worker-organizations.md) | GET |  |

### Timesheet Entries

| Action | Method | Description |
| --- | --- | --- |
| [Create Timesheet Entry](actions/create-timesheet-entry.md) | POST | Create a worker time block in Workday Time Tracking for a specific worker using either quantity-based or clock-in and clock-out entry… |
| [List Worker Time Blocks](actions/list-worker-time-blocks.md) | GET | List worker time blocks from Workday Time Tracking so you can review timesheet-style entries by worker, date range, status, project, or… |
| [Update Timesheet Entry](actions/update-timesheet-entry.md) | PUT | Update an existing worker time block in Workday Time Tracking for a specific worker and time block ID. |

