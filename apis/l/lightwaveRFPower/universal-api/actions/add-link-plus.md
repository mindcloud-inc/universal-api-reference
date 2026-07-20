# LightwaveRF Power: Add LinkPlus

Adds a Link Plus device in LightwaveRF Power.

```
POST https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/add-link-plus
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LightwaveRF Power `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/add-link-plus" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "destinationId": "string",
  "authType": "string",
  "rootGroupId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/add-link-plus', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "destinationId": "string",
    "authType": "string",
    "rootGroupId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `destinationId` | string | yes | The destination identifier used when adding a LinkPlus hub. |
| `authType` | string | yes | The authentication type for the LinkPlus pairing request. |
| `rootGroupId` | string | yes | The root structure group identifier that should own the LinkPlus hub. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deviceId": "string",
      "name": "Ava Chen",
      "rootGroupId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deviceId` | string |  |
| `name` | string |  |
| `rootGroupId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native LightwaveRF Power API, this operation is `POST /v1/linkplus/add` (base URL `https://publicapi.lightwaverf.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-link-plus.md) for the provider-specific parameters and requirements.

