# Globalping: Create Ping Measurement

Creates a ping measurement in Globalping.

```
POST https://connect.mindcloud.co/v1/universal/globalping/latest/actions/create-ping-measurement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Globalping `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/globalping/latest/actions/create-ping-measurement" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "target": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/globalping/latest/actions/create-ping-measurement', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "target": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `target` | string | yes | A publicly reachable hostname or IP address to measure. |
| `limit` | number | no | Maximum number of probes to run. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "probesCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Created measurement identifier. |
| `probesCount` | number | Number of probes assigned to the new measurement. |

## Native endpoint

Through the native Globalping API, this operation is `POST /v1/measurements` (base URL `https://api.globalping.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ping-measurement.md) for the provider-specific parameters and requirements.

