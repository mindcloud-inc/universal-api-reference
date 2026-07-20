# Statsig: Create Autotune

Creates an autotune in Statsig.

```
POST https://connect.mindcloud.co/v1/universal/statsig/latest/actions/create-autotune-post-console-v1-autotunes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/create-autotune-post-console-v1-autotunes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variants": "string",
  "successEvent": "string",
  "explorationWindow": "string",
  "attributionWindow": "string",
  "winnerThreshold": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statsig/latest/actions/create-autotune-post-console-v1-autotunes', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variants": "string",
    "successEvent": "string",
    "explorationWindow": "string",
    "attributionWindow": "string",
    "winnerThreshold": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Request body field. |
| `variants` | list | yes | Request body field. |
| `successEvent` | string | yes | Request body field. |
| `successEventValue` | string | no | Request body field. |
| `explorationWindow` | string | yes | Request body field. |
| `attributionWindow` | string | yes | Request body field. |
| `attributionWindowUnit` | string | no | Request body field. |
| `explorationWindowRate` | number | no | Request body field. |
| `longtermExplorationAllocation` | number | no | Request body field. |
| `winnerThreshold` | string | yes | Request body field. |
| `metadataField` | string | no | Request body field. |
| `higherIsBetter` | boolean | no | Request body field. |
| `isContextual` | boolean | no | Request body field. |
| `metricSourceID` | string | no | Request body field. |
| `linkedExperimentName` | string | no | Request body field. |
| `goalRichText` | string | no | Request body field. |
| `optimizationParameter` | string | no | Request body field. |
| `valueColumn` | string | no | Request body field. |
| `featureList` | list | no | Request body field. |
| `name` | string | yes | Request body field. |
| `idType` | string | no | Request body field. |

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

Through the native Statsig API, this operation is `POST /console/v1/autotunes` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-autotune-post-console-v1-autotunes.md) for the provider-specific parameters and requirements.

