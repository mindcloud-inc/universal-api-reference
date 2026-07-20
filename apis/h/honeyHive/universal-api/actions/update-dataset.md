# HoneyHive: Update Dataset

Updates an existing dataset in HoneyHive.

```
PUT https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/update-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HoneyHive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/update-dataset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datasetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/update-dataset', {
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
| `datasetId` | string | yes | Dataset ID to update. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native HoneyHive API returns.

## Native endpoint

Through the native HoneyHive API, this operation is `PUT /datasets` (base URL `https://api.honeyhive.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-dataset.md) for the provider-specific parameters and requirements.

