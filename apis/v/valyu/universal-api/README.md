# <img src="https://images.mindcloud.co/apps/icons/valyu-network-logo_1777053056281.jpeg" alt="Valyu logo" width="28" height="28"> Valyu: Universal API

Search the web, extract content, answer questions, and run research

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/valyu/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.valyu.ai
- **Vendor API docs:** https://docs.valyu.ai/home

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Datasources](actions/list-datasources.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/valyu/latest/actions/list-datasources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Answer

| Action | Method | Description |
| --- | --- | --- |
| [Answer Query](actions/answer-query.md) | GET |  |

### Content Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Contents Job](actions/create-contents-job.md) | POST |  |

### Content Result

| Action | Method | Description |
| --- | --- | --- |
| [Extract Contents](actions/extract-contents.md) | GET |  |
| [Get Contents Job Status](actions/get-contents-job-status.md) | GET |  |

### Datasource

| Action | Method | Description |
| --- | --- | --- |
| [List Datasources](actions/list-datasources.md) | GET |  |

### Datasource Category

| Action | Method | Description |
| --- | --- | --- |
| [List Datasource Categories](actions/list-datasource-categories.md) | GET |  |

### Deepresearch Task

| Action | Method | Description |
| --- | --- | --- |
| [Create DeepResearch Task](actions/create-deep-research-task.md) | POST |  |
| [Get DeepResearch Task Status](actions/get-deep-research-task-status.md) | GET |  |
| [List DeepResearch Tasks](actions/list-deep-research-tasks.md) | GET |  |
| [Update DeepResearch Task](actions/update-deep-research-task.md) | PUT |  |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search](actions/search.md) | GET |  |

