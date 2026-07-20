# LangChain: Update Dataset



```
PUT https://connect.mindcloud.co/v1/universal/langChain/latest/actions/update-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LangChain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/langChain/latest/actions/update-dataset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datasetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/langChain/latest/actions/update-dataset', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datasetId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datasetId` | string | yes | Dataset identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "data_type": "string",
      "description": "string",
      "externally_managed": true,
      "id": "string",
      "inputs_schema_definition": {},
      "name": "Ava Chen",
      "outputs_schema_definition": {},
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
| `created_at` | date | Creation timestamp. |
| `data_type` | string | Dataset storage type. |
| `description` | string | Dataset description. |
| `externally_managed` | boolean | Whether the dataset is externally managed. |
| `id` | string | Dataset UUID. |
| `inputs_schema_definition` | object | Optional input schema. |
| `name` | string | Dataset name. |
| `outputs_schema_definition` | object | Optional output schema. |
| `tenant_id` | string | Workspace UUID. |
| `transformations` | object | Optional transformation settings. |

## Native endpoint

Through the native LangChain API, this operation is `PATCH /api/v1/datasets/:datasetId` (base URL `https://api.smith.langchain.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-dataset.md) for the provider-specific parameters and requirements.

