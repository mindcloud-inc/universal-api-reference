# Datastreamer: Search Work Items



```
GET https://connect.mindcloud.co/v1/universal/datastreamer/latest/actions/search-work-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datastreamer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datastreamer/latest/actions/search-work-items?connectionId=$CONNECTION_ID&query=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datastreamer/latest/actions/search-work-items?${params}`, {
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
| `query` | object | yes | Search request payload for work items. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Datastreamer API returns.

## Native endpoint

Through the native Datastreamer API, this operation is `POST /api/pipelines/work-items/search` (base URL `https://api.platform.datastreamer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-work-items.md) for the provider-specific parameters and requirements.

