# Rachio Smart Lighting Controller: Set Lighting Zone Dimming Levels



```
PUT https://connect.mindcloud.co/v1/universal/rachioSmartLightingController/latest/actions/set-lighting-zone-dimming-levels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rachio Smart Lighting Controller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rachioSmartLightingController/latest/actions/set-lighting-zone-dimming-levels" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rachioSmartLightingController/latest/actions/set-lighting-zone-dimming-levels', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dimming_percent` | string | no |  |
| `id` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rachio Smart Lighting Controller API returns.

## Native endpoint

Through the native Rachio Smart Lighting Controller API, this operation is `PUT https://cloud-rest.rach.io/lighting/setLightingZoneDimmingLevels` (base URL `https://cloud-rest.rach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-lighting-zone-dimming-levels.md) for the provider-specific parameters and requirements.

