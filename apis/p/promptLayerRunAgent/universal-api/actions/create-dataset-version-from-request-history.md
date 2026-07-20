# PromptLayer Run Agent: Create Dataset Version From Request History

Creates a dataset version in PromptLayer from request history.

```
POST https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/create-dataset-version-from-request-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/create-dataset-version-from-request-history" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datasetGroupId": "20196"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/create-dataset-version-from-request-history', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datasetGroupId": "20196"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datasetGroupId` | number | yes | ID of the dataset group where the new version will be created. Example: `20196`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | no | Filter to a single request log by its numeric id. Example: `4742717447`. |
| `limit` | number | no | Maximum number of request logs to include. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dataset_group_id": 1,
      "dataset_id": 1,
      "message": "string",
      "success": true,
      "version_number": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataset_group_id` | number |  |
| `dataset_id` | number |  |
| `message` | string |  |
| `success` | boolean |  |
| `version_number` | number |  |

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `POST /api/public/v2/dataset-versions/from-filter-params` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-dataset-version-from-request-history.md) for the provider-specific parameters and requirements.

