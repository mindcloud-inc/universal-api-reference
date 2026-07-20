# Webcrawler API: Get Feed JSON

Retrieves feed changes in JSON Feed format from Webcrawler API.

```
GET https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/get-feed-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webcrawler API `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/get-feed-json?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/get-feed-json?${params}`, {
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
| `id` | string | yes | Feed identifier returned by List Feeds. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Webcrawler API API returns.

## Native endpoint

Through the native Webcrawler API API, this operation is `GET /v2/feed/:id/json` (base URL `https://api.webcrawlerapi.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-feed-json.md) for the provider-specific parameters and requirements.

