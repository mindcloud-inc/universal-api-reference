# PromptLayer Run Agent Universal API Examples

These examples use the MindCloud API key and PromptLayer Run Agent connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Agents

Retrieves a list of workflows from PromptLayer.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/list-agents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/list-agents?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Agents action reference](actions/list-agents.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/promptLayerRunAgent/latest/actions/list-agents).

## Add Column To Evaluation Pipeline

Adds a column to a PromptLayer evaluation pipeline.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/add-column-to-evaluation-pipeline" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reportId": "45405",
  "columnType": "HUMAN",
  "name": "Human Rating 2",
  "configuration": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/add-column-to-evaluation-pipeline', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reportId": "45405",
    "columnType": "HUMAN",
    "name": "Human Rating 2",
    "configuration": "[object Object]"
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
      "report_column": {},
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add Column To Evaluation Pipeline action reference](actions/add-column-to-evaluation-pipeline.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/promptLayerRunAgent/latest/actions/add-column-to-evaluation-pipeline).
