# Adafruit IO: Get Data Point

Retrieves a data point from an Adafruit IO feed.

```
GET https://connect.mindcloud.co/v1/universal/adafruitIO/latest/actions/get-data-point
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Adafruit IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adafruitIO/latest/actions/get-data-point?connectionId=$CONNECTION_ID&feedKey=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "feedKey": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adafruitIO/latest/actions/get-data-point?${params}`, {
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
| `id` | string | yes |  |
| `include` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Adafruit IO API returns.

## Native endpoint

Through the native Adafruit IO API, this operation is `GET /{{credentials.username}}/feeds/:feed_key/data/:id` (base URL `https://io.adafruit.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-point.md) for the provider-specific parameters and requirements.

