# <img src="https://mindcloud.imgix.net/apps/icons/id-gk-epyyg-1770742625103_1770742631169.jpeg" alt="Tinybird logo" width="28" height="28"> Tinybird: Universal API

Tinybird: Query data, manage sources, and build pipelines

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tinybird/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 37
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.tinybird.co
- **Vendor API docs:** https://www.tinybird.co/docs/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Data Sources](actions/list-data-sources.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/list-data-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (37)

### Data Source

| Action | Method | Description |
| --- | --- | --- |
| [Alter Data Source](actions/alter-data-source.md) | PUT |  |
| [Append Data](actions/append-data.md) | POST |  |
| [Create Data Source](actions/create-data-source.md) | POST |  |
| [Delete Data Source](actions/delete-data-source.md) | DELETE |  |
| [Get Data Source](actions/get-data-source.md) | GET |  |
| [List Data Sources](actions/list-data-sources.md) | GET |  |
| [Replace Data](actions/replace-data.md) | PUT |  |
| [Truncate Data Source](actions/truncate-data-source.md) | DELETE |  |

### Environment Variable

| Action | Method | Description |
| --- | --- | --- |
| [Create Environment Variable](actions/create-environment-variable.md) | POST |  |
| [Delete Environment Variable](actions/delete-environment-variable.md) | DELETE |  |
| [Get Environment Variable](actions/get-environment-variable.md) | GET |  |
| [List Environment Variables](actions/list-environment-variables.md) | GET |  |
| [Update Environment Variable](actions/update-environment-variable.md) | PUT |  |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Ingest Events](actions/ingest-events.md) | POST |  |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Job](actions/cancel-job.md) | PUT |  |
| [Delete Matching Data](actions/delete-matching-data.md) | DELETE |  |
| [Get Job](actions/get-job.md) | GET |  |
| [List Jobs](actions/list-jobs.md) | GET |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Data File](actions/analyze-data-file.md) | POST |  |

### Pipe

| Action | Method | Description |
| --- | --- | --- |
| [Add Pipe Node](actions/add-pipe-node.md) | POST |  |
| [Create Pipe](actions/create-pipe.md) | POST |  |
| [Delete Pipe](actions/delete-pipe.md) | DELETE |  |
| [Delete Pipe Node](actions/delete-pipe-node.md) | DELETE |  |
| [Get Pipe](actions/get-pipe.md) | GET |  |
| [List Pipes](actions/list-pipes.md) | GET |  |
| [Update Pipe](actions/update-pipe.md) | PUT |  |
| [Update Pipe Node](actions/update-pipe-node.md) | PUT |  |

### Query

| Action | Method | Description |
| --- | --- | --- |
| [Execute SQL Query](actions/execute-sql-query.md) | GET |  |
| [Execute SQL Query (GET)](actions/execute-sql-query-get.md) | GET |  |
| [Query Pipe](actions/query-pipe.md) | GET |  |
| [Query Pipe (POST)](actions/query-pipe-post.md) | GET |  |

### Static Token

| Action | Method | Description |
| --- | --- | --- |
| [Create Static Token](actions/create-static-token.md) | POST |  |
| [Delete Static Token](actions/delete-static-token.md) | DELETE |  |
| [Get Static Token](actions/get-static-token.md) | GET |  |
| [List Static Tokens](actions/list-static-tokens.md) | GET |  |
| [Refresh Static Token](actions/refresh-static-token.md) | PUT |  |
| [Update Static Token](actions/update-static-token.md) | PUT |  |

