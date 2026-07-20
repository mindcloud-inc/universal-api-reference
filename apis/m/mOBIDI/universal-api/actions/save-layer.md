# MOBIDI: Save Layer

Creates or updates a layer in MOBIDI.

```
POST https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/save-layer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MOBIDI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/save-layer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "layer": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/save-layer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "layer": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `layer` | string | yes | Serialized MobidiLayer payload. |
| `isNewLayer` | boolean | no | Whether the layer is new. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `layerIdControl` | boolean | no | Whether to enforce layer ID control. Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MOBIDI API returns.

## Native endpoint

Through the native MOBIDI API, this operation is `POST /MobidiWorkspaceManagerHandler` (base URL `https://servis2.dece.com.tr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-layer.md) for the provider-specific parameters and requirements.

