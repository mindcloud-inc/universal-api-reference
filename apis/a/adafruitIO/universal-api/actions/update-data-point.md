# Adafruit IO: Update Data Point

Updates a data point in an Adafruit IO feed.

```
PUT https://connect.mindcloud.co/v1/universal/adafruitIO/latest/actions/update-data-point
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Adafruit IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/adafruitIO/latest/actions/update-data-point" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "feedKey": "string",
  "id": "string",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/adafruitIO/latest/actions/update-data-point', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "feedKey": "string",
    "id": "string",
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createdAt` | date | no |  |
| `ele` | number | no |  |
| `feedKey` | string | yes |  |
| `id` | string | yes |  |
| `lat` | number | no |  |
| `lon` | number | no |  |
| `value` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Adafruit IO API returns.

## Native endpoint

Through the native Adafruit IO API, this operation is `PUT /{{credentials.username}}/feeds/:feed_key/data/:id` (base URL `https://io.adafruit.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-data-point.md) for the provider-specific parameters and requirements.

