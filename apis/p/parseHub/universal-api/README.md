# <img src="https://images.mindcloud.co/apps/icons/parse-hub_1775489629632.png" alt="ParseHub logo" width="28" height="28"> ParseHub: Universal API

ParseHub lets you manage scraping projects, run them, inspect run status, and fetch extracted data through the official ParseHub API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/parseHub/latest
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.parsehub.com
- **Vendor API docs:** https://www.parsehub.com/docs/ref/api/v2/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parseHub/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Last Ready Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Last Ready Data (JSON)](actions/get-last-ready-data-json.md) | GET |  |

### Last Ready Data Export

| Action | Method | Description |
| --- | --- | --- |
| [Get Last Ready Data (CSV)](actions/get-last-ready-data-csv.md) | GET |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |

### Run

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Run](actions/cancel-run.md) | PUT |  |
| [Delete Run](actions/delete-run.md) | DELETE |  |
| [Get Run](actions/get-run.md) | GET |  |
| [Run Project](actions/run-project.md) | POST |  |

### Run Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Run Data (JSON)](actions/get-run-data-json.md) | GET |  |

### Run Data Export

| Action | Method | Description |
| --- | --- | --- |
| [Get Run Data (CSV)](actions/get-run-data-csv.md) | GET |  |

