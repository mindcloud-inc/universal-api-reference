# Adafruit IO: Add Feed to Group

Adds a feed to an Adafruit IO group.

```
PUT https://connect.mindcloud.co/v1/universal/adafruitIO/latest/actions/add-feed-to-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Adafruit IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/adafruitIO/latest/actions/add-feed-to-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "feedKey": "string",
  "groupKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/adafruitIO/latest/actions/add-feed-to-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "feedKey": "string",
    "groupKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `feedKey` | string | yes |  |
| `groupKey` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Adafruit IO API returns.

## Native endpoint

Through the native Adafruit IO API, this operation is `POST /{{credentials.username}}/groups/:group_key/add` (base URL `https://io.adafruit.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-feed-to-group.md) for the provider-specific parameters and requirements.

