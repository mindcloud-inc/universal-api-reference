# EMnify: Set Endpoint Data Quota

Sets a new data quota for an endpoint in EMnify.

```
POST https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/set-endpoint-data-quota
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EMnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/set-endpoint-data-quota" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "authToken": "Paste the auth_token from Retrieve Authentication Token",
  "endpointId": "18811970",
  "status.id": "1",
  "volume": "100",
  "expiryDate": "2026-03-27 17:00:00",
  "actionOnExhaustion.id": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/set-endpoint-data-quota', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "authToken": "Paste the auth_token from Retrieve Authentication Token",
    "endpointId": "18811970",
    "status.id": "1",
    "volume": "100",
    "expiryDate": "2026-03-27 17:00:00",
    "actionOnExhaustion.id": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `authToken` | string | yes | Auth token from Retrieve Authentication Token. Example: `Paste the auth_token from Retrieve Authentication Token`. |
| `endpointId` | number | yes | Endpoint ID to configure. Example: `18811970`. |
| `status.id` | number | yes | Quota status ID. Example: `1`. |
| `volume` | number | yes | Remaining quota volume in MB. Example: `100`. |
| `expiryDate` | string | yes | Quota expiry timestamp. Example: `2026-03-27 17:00:00`. |
| `actionOnExhaustion.id` | number | yes | Action ID to execute when the quota is exhausted. Example: `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `autoRefill` | number | no | Whether the quota should auto-refill daily. Example: `0`. |
| `thresholdPercentage` | number | no | Remaining quota percentage threshold for events. Example: `15`. |
| `lastVolumeAdded` | number | no | Last added quota volume. Example: `50`. |
| `lastStatusChangeDate` | string | no | Quota status change timestamp. Example: `2026-03-20 17:00:00`. |
| `thresholdVolume` | number | no | Remaining quota volume threshold for events. Example: `20`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EMnify API returns.

## Native endpoint

Through the native EMnify API, this operation is `POST /endpoint/:endpoint_id/quota/data` (base URL `https://cdn.emnify.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-endpoint-data-quota.md) for the provider-specific parameters and requirements.

