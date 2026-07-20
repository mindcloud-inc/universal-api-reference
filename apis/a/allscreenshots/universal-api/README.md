# <img src="https://images.mindcloud.co/apps/icons/test_1782738832338.png" alt="Allscreenshots logo" width="28" height="28"> Allscreenshots: Universal API

Capture website screenshots, run bulk jobs, and manage recurring captures

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/allscreenshots/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://allscreenshots.com
- **Vendor API docs:** https://docs.allscreenshots.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Schedules](actions/list-schedules.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/list-schedules?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Bulk Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Bulk Job](actions/create-bulk-job.md) | POST | Creates a bulk screenshot job for multiple URLs in Allscreenshots. |
| [Get Bulk Job Status](actions/get-bulk-job-status.md) | GET | Retrieves the status of a bulk screenshot job in Allscreenshots. |

### Composition

| Action | Method | Description |
| --- | --- | --- |
| [Create Composition](actions/create-composition.md) | POST | Creates a single image from multiple screenshots in Allscreenshots. |

### Schedule

| Action | Method | Description |
| --- | --- | --- |
| [List Schedules](actions/list-schedules.md) | GET | Retrieves recurring screenshot schedules from Allscreenshots. |

### Screenshot

| Action | Method | Description |
| --- | --- | --- |
| [Create Screenshot](actions/create-screenshot.md) | POST | Creates a new website capture in Allscreenshots. |

### Screenshot Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Async Screenshot Job](actions/create-async-screenshot-job.md) | POST | Creates a new async screenshot job in Allscreenshots. |
| [Get Screenshot Job Status](actions/get-screenshot-job-status.md) | GET | Retrieves the status of an async screenshot job in Allscreenshots. |

### Screenshot Output

| Action | Method | Description |
| --- | --- | --- |
| [Get Screenshot Job Output Result](actions/get-screenshot-job-output-result.md) | GET | Retrieves a specific output from an async screenshot job in Allscreenshots. |

### Screenshot Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Screenshot Job Result](actions/get-screenshot-job-result.md) | GET | Retrieves the completed result of an async screenshot job in Allscreenshots. |

