# Chargeblast: Upload IP Data

Uploads IP data to Chargeblast.

```
POST https://connect.mindcloud.co/v1/universal/chargeblast/latest/actions/upload-ip-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chargeblast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chargeblast/latest/actions/upload-ip-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "ip": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chargeblast/latest/actions/upload-ip-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "ip": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | The customer email associated with the IP signal. |
| `ip` | string | yes | The customer IP address. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Chargeblast API returns.

## Native endpoint

Through the native Chargeblast API, this operation is `POST /api/v2/track` (base URL `https://api.chargeblast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-ip-data.md) for the provider-specific parameters and requirements.

