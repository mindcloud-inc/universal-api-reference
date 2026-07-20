# LightwaveRF Lighting: Batch Read Historical Data

Retrieves historical data for multiple features from LightwaveRF Lighting.

```
GET https://connect.mindcloud.co/v1/universal/lightwaveRFLighting/latest/actions/batch-read-historical-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LightwaveRF Lighting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightwaveRFLighting/latest/actions/batch-read-historical-data?connectionId=$CONNECTION_ID&devices%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "devices[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightwaveRFLighting/latest/actions/batch-read-historical-data?${params}`, {
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
| `devices[]` | array<object> | yes | The list of devices whose historical data should be read. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `start` | number | no | The earliest timestamp to include in the batch historical data query. |
| `end` | number | no | The latest timestamp to include in the batch historical data query. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LightwaveRF Lighting API returns.

## Native endpoint

Through the native LightwaveRF Lighting API, this operation is `POST /v1/data` (base URL `https://publicapi.lightwaverf.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-read-historical-data.md) for the provider-specific parameters and requirements.

