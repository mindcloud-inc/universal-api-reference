# LightwaveRF Lighting: Add Device

Adds a device to LightwaveRF Lighting.

```
POST https://connect.mindcloud.co/v1/universal/lightwaveRFLighting/latest/actions/add-device
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LightwaveRF Lighting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lightwaveRFLighting/latest/actions/add-device" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "type": "string",
  "destinationId": "string",
  "productCode": "string",
  "manufacturerCode": "string",
  "parentGroups": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lightwaveRFLighting/latest/actions/add-device', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "type": "string",
    "destinationId": "string",
    "productCode": "string",
    "manufacturerCode": "string",
    "parentGroups": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The new device name. |
| `type` | string | yes | The LightwaveRF device type. |
| `destinationId` | string | yes | The destination identifier the device should be added to. |
| `productCode` | string | yes | The LightwaveRF product code for the device. |
| `manufacturerCode` | string | yes | The manufacturer code for the device. |
| `parentGroups` | string | yes | The parent group identifiers that should contain the device. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LightwaveRF Lighting API returns.

## Native endpoint

Through the native LightwaveRF Lighting API, this operation is `POST /v1/device/add` (base URL `https://publicapi.lightwaverf.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-device.md) for the provider-specific parameters and requirements.

