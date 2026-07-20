# LightwaveRF Power: Get Feature

Retrieves a feature from LightwaveRF Power.

```
GET https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/get-feature
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LightwaveRF Power `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/get-feature?connectionId=$CONNECTION_ID&featureId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "featureId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/get-feature?${params}`, {
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
| `featureId` | string | yes | The LightwaveRF feature identifier to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deviceId": "string",
      "featureId": "string",
      "name": "Ava Chen",
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
| `deviceId` | string |  |
| `featureId` | string |  |
| `name` | string |  |
| `type` | string |  |
| `value` | number |  |
| `writable` | boolean |  |

## Native endpoint

Through the native LightwaveRF Power API, this operation is `GET /v1/feature/{featureId}` (base URL `https://publicapi.lightwaverf.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feature.md) for the provider-specific parameters and requirements.

