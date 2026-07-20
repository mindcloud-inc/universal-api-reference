# <img src="https://images.mindcloud.co/apps/icons/download_1754442602171.png" alt="Google BigQuery logo" width="28" height="28"> Google BigQuery: Universal API

Google BigQuery through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/googleBigQuery/latest
- **Category:** Business Intelligence / Data Warehouse
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor API docs:** https://bigquery.googleapis.com/$discovery/rest?version=v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Query](actions/query.md):

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleBigQuery/latest/actions/query" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": "string"
}'
```

## Actions (1)

### Query

| Action | Method | Description |
| --- | --- | --- |
| [Query](actions/query.md) | PUT |  |

