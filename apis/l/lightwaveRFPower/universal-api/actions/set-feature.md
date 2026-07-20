# LightwaveRF Power: Set Feature

Updates a feature in LightwaveRF Power.

```
PUT https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/set-feature
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LightwaveRF Power `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/set-feature" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "featureId": "string",
  "value": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/set-feature', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "featureId": "string",
    "value": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `featureId` | string | yes | The LightwaveRF feature identifier to update. |
| `value` | number | yes | The numeric value to write to the feature. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "featureId": "string",
      "success": true,
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `featureId` | string |  |
| `success` | boolean |  |
| `value` | number |  |

## Native endpoint

Through the native LightwaveRF Power API, this operation is `POST /v1/feature/{featureId}` (base URL `https://publicapi.lightwaverf.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-feature.md) for the provider-specific parameters and requirements.

