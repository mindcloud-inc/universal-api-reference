# <img src="https://images.mindcloud.co/apps/icons/favicon-www-workday-com-48x48_1782311713391.png" alt="Workday logo" width="28" height="28"> Workday: Universal API

Workday scaffold based on the attached Time Tracking v5 OpenAPI spec. Current scope covers worker retrieval plus worker time block retrieval and create/update shells for timesheet-style entries.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/workday/latest
- **Category:** Human Resources / HRIS
- **Actions:** 6
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

## Actions (6)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Get Token](actions/get-token.md) | GET | Exchange a refresh token for a new Workday access token. |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Profiles](actions/get-job-profiles.md) | GET |  |
| [Get Worker](actions/get-worker.md) | GET | Get a single worker from Workday Time Tracking by Workday worker ID. |
| [Get Workers](actions/get-workers.md) | GET | List workers from Workday Time Tracking with optional name or worker ID search, visibility filtering, and pagination. |
| [Get Workers History](actions/get-workers-history.md) | GET |  |
| [List Worker Organizations](actions/list-worker-organizations.md) | GET |  |

