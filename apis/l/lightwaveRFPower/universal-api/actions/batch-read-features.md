# LightwaveRF Power: Batch Read Features

Retrieves multiple features from LightwaveRF Power.

```
GET https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/batch-read-features
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LightwaveRF Power `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/batch-read-features?connectionId=$CONNECTION_ID&features%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "features[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/batch-read-features?${params}`, {
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
| `features[]` | array<object> | yes | The list of feature identifiers to read in one request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "featureId": "string",
      "type": "string",
      "value": 1,
      "writable": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `featureId` | string |  |
| `type` | string |  |
| `value` | number |  |
| `writable` | boolean |  |

## Native endpoint

Through the native LightwaveRF Power API, this operation is `POST /v1/features/read` (base URL `https://publicapi.lightwaverf.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-read-features.md) for the provider-specific parameters and requirements.

