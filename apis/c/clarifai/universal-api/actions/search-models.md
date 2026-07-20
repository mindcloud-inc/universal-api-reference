# Clarifai: Search Models

Finds models in Clarifai by model ID or name.

```
GET https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/search-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clarifai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/search-models?connectionId=$CONNECTION_ID&appId=string&model_query=%5Bobject%20Object%5D&model_query.name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string",
  "model_query": "[object Object]",
  "model_query.name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/search-models?${params}`, {
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
| `model_query` | object | yes | Model search query. |
| `model_query.name` | string | yes | Model ID or name to search for. |
| `model_query.model_type_id` | string | no | Filter search by model type ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Clarifai API returns.

## Native endpoint

Through the native Clarifai API, this operation is `POST /v2/users/me/apps/:appId/models/searches` (base URL `https://api.clarifai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-models.md) for the provider-specific parameters and requirements.

