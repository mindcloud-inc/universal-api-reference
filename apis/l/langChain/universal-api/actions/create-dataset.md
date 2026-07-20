# LangChain: Create Dataset



```
POST https://connect.mindcloud.co/v1/universal/langChain/latest/actions/create-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LangChain `connectionId` ([setup](../authentication.md)).

## Example request

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



## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseline_experiment_id` | string | Optional baseline experiment UUID. |
| `created_at` | date | Creation timestamp. |
| `data_type` | string | Dataset storage type. |
| `description` | string | Dataset description. |
| `example_count` | number | Example count. |
| `externally_managed` | boolean | Whether the dataset is externally managed. |
| `id` | string | Dataset UUID. |
| `inputs_schema_definition` | object | Optional input schema. |
| `last_session_start_time` | date | Last session start time. |
| `metadata` | object | Custom metadata. |
| `modified_at` | date | Last update timestamp. |
| `name` | string | Dataset name. |
| `outputs_schema_definition` | object | Optional output schema. |
| `session_count` | number | Session count. |
| `tenant_id` | string | Workspace UUID. |
| `transformations` | object | Optional transformation settings. |

## Native endpoint

Through the native LangChain API, this operation is `POST /api/v1/datasets` (base URL `https://api.smith.langchain.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-dataset.md) for the provider-specific parameters and requirements.

