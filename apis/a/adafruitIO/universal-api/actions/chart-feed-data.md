# Adafruit IO: Chart Feed Data

Retrieves charted data from an Adafruit IO feed.

```
GET https://connect.mindcloud.co/v1/universal/adafruitIO/latest/actions/chart-feed-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Adafruit IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adafruitIO/latest/actions/chart-feed-data?connectionId=$CONNECTION_ID&feedKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "feedKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adafruitIO/latest/actions/chart-feed-data?${params}`, {
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
| `endTime` | date | no |  |
| `feedKey` | string | yes |  |
| `field` | string | no |  |
| `hours` | number | no |  |
| `raw` | boolean | no |  |
| `resolution` | number | no |  |
| `startTime` | date | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Adafruit IO API returns.

## Native endpoint

Through the native Adafruit IO API, this operation is `GET /{{credentials.username}}/feeds/:feed_key/data/chart` (base URL `https://io.adafruit.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/chart-feed-data.md) for the provider-specific parameters and requirements.

