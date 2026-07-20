# Parallel Web Systems Universal API Examples

These examples use the MindCloud API key and Parallel Web Systems connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Monitors



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/list-monitors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/list-monitors?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "cadence": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "frequency": "string",
      "include_backfill": true,
      "last_run_at": "2026-05-07T12:00:00.000Z",
      "monitor_id": "string",
      "query": "string",
      "status": "string",
      "webhook": {
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

See the full [List Monitors action reference](actions/list-monitors.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/parallelWebSystems/latest/actions/list-monitors).

## Add Enrichment to FindAll Run



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/add-enrichment-to-find-all-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "findallId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/add-enrichment-to-find-all-run', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "findallId": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "enrichments": {
        "processor": "string"
      },
      "entity_type": "string",
      "generator": "string",
      "match_conditions": {
        "description": "string",
        "name": "Ava Chen"
      },
      "match_limit": 1,
      "objective": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Enrichment to FindAll Run action reference](actions/add-enrichment-to-find-all-run.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/parallelWebSystems/latest/actions/add-enrichment-to-find-all-run).
