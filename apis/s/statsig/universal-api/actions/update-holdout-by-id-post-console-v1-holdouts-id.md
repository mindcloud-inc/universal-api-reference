# Statsig: Update holdout by id

Updates a holdout in Statsig by ID.

```
PUT https://connect.mindcloud.co/v1/universal/statsig/latest/actions/update-holdout-by-id-post-console-v1-holdouts-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/update-holdout-by-id-post-console-v1-holdouts-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "isEnabled": true,
  "description": "string",
  "passPercentage": 1,
  "gateIDs": "string",
  "experimentIDs": "string",
  "layerIDs": "string",
  "isGlobal": true,
  "targetingGateID": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statsig/latest/actions/update-holdout-by-id-post-console-v1-holdouts-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "isEnabled": true,
    "description": "string",
    "passPercentage": 1,
    "gateIDs": "string",
    "experimentIDs": "string",
    "layerIDs": "string",
    "isGlobal": true,
    "targetingGateID": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | id |
| `isEnabled` | boolean | yes | Request body field. |
| `description` | string | yes | Request body field. |
| `passPercentage` | number | yes | Request body field. |
| `gateIDs` | list | yes | Request body field. |
| `experimentIDs` | list | yes | Request body field. |
| `layerIDs` | list | yes | Request body field. |
| `isGlobal` | boolean | yes | Request body field. |
| `targetingGateID` | string | yes | Request body field. |
| `monitoringMetrics` | list | no | Request body field. |

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

Through the native Statsig API, this operation is `POST /console/v1/holdouts/{id}` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-holdout-by-id-post-console-v1-holdouts-id.md) for the provider-specific parameters and requirements.

