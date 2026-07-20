# LightwaveRF Lighting: Batch Write Features

Updates multiple features in LightwaveRF Lighting.

```
PUT https://connect.mindcloud.co/v1/universal/lightwaveRFLighting/latest/actions/batch-write-features
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LightwaveRF Lighting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lightwaveRFLighting/latest/actions/batch-write-features" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "features[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lightwaveRFLighting/latest/actions/batch-write-features', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "features[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `features[]` | array<object> | yes | The list of feature writes to apply in one request. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LightwaveRF Lighting API returns.

## Native endpoint

Through the native LightwaveRF Lighting API, this operation is `POST /v1/features/write` (base URL `https://publicapi.lightwaverf.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-write-features.md) for the provider-specific parameters and requirements.

