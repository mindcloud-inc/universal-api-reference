# Adafruit IO: Remove Feed from Group

Removes a feed from an Adafruit IO group.

```
DELETE https://connect.mindcloud.co/v1/universal/adafruitIO/latest/actions/remove-feed-from-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Adafruit IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/adafruitIO/latest/actions/remove-feed-from-group?connectionId=$CONNECTION_ID&feedKey=string&groupKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "feedKey": "string",
  "groupKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adafruitIO/latest/actions/remove-feed-from-group?${params}`, {
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
| `feedKey` | string | yes |  |
| `groupKey` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Adafruit IO API returns.

## Native endpoint

Through the native Adafruit IO API, this operation is `POST /{{credentials.username}}/groups/:group_key/remove` (base URL `https://io.adafruit.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-feed-from-group.md) for the provider-specific parameters and requirements.

