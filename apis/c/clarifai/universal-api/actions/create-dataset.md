# Clarifai: Create Dataset

Creates a new dataset in Clarifai.

```
POST https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/create-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clarifai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/create-dataset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "datasets[]": [
    {}
  ],
  "datasets[].id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/create-dataset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "datasets[]": [{}],
    "datasets[].id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | Clarifai app ID. |
| `datasets[]` | array<object> | yes | Datasets to create. |
| `datasets[].id` | string | yes | Dataset ID. |
| `datasets[].description` | string | no | Dataset description. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Clarifai API returns.

## Native endpoint

Through the native Clarifai API, this operation is `POST /v2/users/me/apps/:appId/datasets` (base URL `https://api.clarifai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-dataset.md) for the provider-specific parameters and requirements.

