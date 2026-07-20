# Dappier: Search Real Time Data

Retrieves a real-time AI search response from Dappier.

```
GET https://connect.mindcloud.co/v1/universal/dappier/latest/actions/search-real-time-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dappier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dappier/latest/actions/search-real-time-data?connectionId=$CONNECTION_ID&aiModelId=am_01j06ytn18ejftedz6dyhz2b15&query=What%20is%20the%20weather%20in%20Austin%20today%3F" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "aiModelId": "am_01j06ytn18ejftedz6dyhz2b15",
  "query": "What is the weather in Austin today?"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dappier/latest/actions/search-real-time-data?${params}`, {
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
| `aiModelId` | string | yes | The ID of the AI model to query. Default: `am_01j06ytn18ejftedz6dyhz2b15`. |
| `query` | string | yes | The query text to be passed to the AI model. Default: `What is the weather in Austin today?`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dappier API returns.

## Native endpoint

Through the native Dappier API, this operation is `POST /app/aimodel/:aiModelId` (base URL `https://api.dappier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-real-time-data.md) for the provider-specific parameters and requirements.

