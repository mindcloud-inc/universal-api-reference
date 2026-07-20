# Statsig: Add Layer Overrides

Adds layer overrides in Statsig.

```
POST https://connect.mindcloud.co/v1/universal/statsig/latest/actions/add-layer-overrides-patch-console-v1-layers-id-overrides
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/add-layer-overrides-patch-console-v1-layers-id-overrides" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "op": "string",
  "conditionalOverrides": "string",
  "idOverrides": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statsig/latest/actions/add-layer-overrides-patch-console-v1-layers-id-overrides', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "op": "string",
    "conditionalOverrides": "string",
    "idOverrides": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | id |
| `op` | string | yes | Request body field. |
| `conditionalOverrides` | list | yes | Request body field. |
| `idOverrides` | list | yes | Request body field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `PATCH /console/v1/layers/{id}/overrides` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-layer-overrides-patch-console-v1-layers-id-overrides.md) for the provider-specific parameters and requirements.

