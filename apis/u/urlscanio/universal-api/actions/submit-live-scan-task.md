# urlscan.io: Submit Live Scan Task



```
POST https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/submit-live-scan-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a urlscan.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/submit-live-scan-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/submit-live-scan-task', {
  method: 'POST',
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
| `scannerId` | string | no | The live scanner node identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `uuid` | string |  |

## Native endpoint

Through the native urlscan.io API, this operation is `POST /api/v1/livescan/{scannerId}/task/` (base URL `https://urlscan.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-live-scan-task.md) for the provider-specific parameters and requirements.

