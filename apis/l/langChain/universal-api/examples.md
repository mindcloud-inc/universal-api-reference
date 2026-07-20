# LangChain Universal API Examples

These examples use the MindCloud API key and LangChain connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Sessions



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langChain/latest/actions/list-sessions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langChain/latest/actions/list-sessions?${params}`, {
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
      "completionCost": {},
      "completionTokens": {},
      "defaultDatasetId": {},
      "description": {},
      "endTime": {},
      "errorRate": {},
      "extra": {},
      "feedbackStats": {},
      "firstTokenP50": {},
      "firstTokenP99": {},
      "id": "string",
      "lastRunStartTime": {},
      "lastRunStartTimeLive": {},
      "latencyP50": {},
      "latencyP99": {},
      "name": "Ava Chen",
      "promptCost": {},
      "promptTokens": {},
      "referenceDatasetId": {},
      "runCount": {},
      "runFacets": {},
      "sessionFeedbackStats": {},
      "startTime": "string",
      "streamingRate": {},
      "tenantId": "string",
      "testRunNumber": {},
      "totalCost": {},
      "totalTokens": {},
      "traceTier": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Sessions action reference](actions/list-sessions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/langChain/latest/actions/list-sessions).

## Create Dataset



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/langChain/latest/actions/create-dataset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/langChain/latest/actions/create-dataset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "baseline_experiment_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "data_type": "string",
      "description": "string",
      "example_count": 1,
      "externally_managed": true,
      "id": "string",
      "inputs_schema_definition": {},
      "last_session_start_time": "2026-05-07T12:00:00.000Z",
      "metadata": {},
      "modified_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "outputs_schema_definition": {},
      "session_count": 1,
      "tenant_id": "string",
      "transformations": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Dataset action reference](actions/create-dataset.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/langChain/latest/actions/create-dataset).
