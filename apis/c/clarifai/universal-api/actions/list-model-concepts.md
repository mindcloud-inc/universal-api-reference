# Clarifai: List Model Concepts

Retrieves model concepts from Clarifai.

```
GET https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/list-model-concepts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clarifai `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/list-model-concepts?connectionId=$CONNECTION_ID&limit=25&offset=0&appId=string&modelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "appId": "string",
  "modelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/list-model-concepts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | Clarifai app ID. |
| `modelId` | string | yes | Clarifai model ID. |
| `versionId` | string | no | Specific model version ID. |
| `search` | string | no | Search term for model concepts. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Clarifai API returns.

## Native endpoint

Through the native Clarifai API, this operation is `GET /v2/users/me/apps/:appId/models/:modelId/concepts` (base URL `https://api.clarifai.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-model-concepts.md) for the provider-specific parameters and requirements.

