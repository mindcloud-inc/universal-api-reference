# Adafruit IO: List Group Feeds

Retrieves feeds from an Adafruit IO group.

```
GET https://connect.mindcloud.co/v1/universal/adafruitIO/latest/actions/list-group-feeds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Adafruit IO `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adafruitIO/latest/actions/list-group-feeds?connectionId=$CONNECTION_ID&limit=25&offset=0&groupKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "groupKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adafruitIO/latest/actions/list-group-feeds?${params}`, {
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
| `groupKey` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Adafruit IO API returns.

## Native endpoint

Through the native Adafruit IO API, this operation is `GET /{{credentials.username}}/groups/:group_key/feeds` (base URL `https://io.adafruit.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-group-feeds.md) for the provider-specific parameters and requirements.

