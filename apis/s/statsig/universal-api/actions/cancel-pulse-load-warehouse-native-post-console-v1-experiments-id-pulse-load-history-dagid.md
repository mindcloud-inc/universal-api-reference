# Statsig: Cancel Pulse Load (Warehouse Native)

Cancels a warehouse-native pulse load in Statsig.

```
POST https://connect.mindcloud.co/v1/universal/statsig/latest/actions/cancel-pulse-load-warehouse-native-post-console-v1-experiments-id-pulse-load-history-dagid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/cancel-pulse-load-warehouse-native-post-console-v1-experiments-id-pulse-load-history-dagid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "dagID": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statsig/latest/actions/cancel-pulse-load-warehouse-native-post-console-v1-experiments-id-pulse-load-history-dagid', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "dagID": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | id |
| `dagID` | string | yes | dagID |

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

Through the native Statsig API, this operation is `POST /console/v1/experiments/{id}/pulse_load_history/{dagID}/cancel` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-pulse-load-warehouse-native-post-console-v1-experiments-id-pulse-load-history-dagid.md) for the provider-specific parameters and requirements.

