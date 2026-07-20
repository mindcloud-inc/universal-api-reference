# Hightouch: Queue IDR Identifiers For Reprocessing

Queues IDR identifiers for reprocessing in Hightouch.

```
POST https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/queue-idr-identifiers-for-reprocessing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hightouch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/queue-idr-identifiers-for-reprocessing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "graphId": "string",
  "identifiers[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/queue-idr-identifiers-for-reprocessing', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "graphId": "string",
    "identifiers[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `graphId` | string | yes | The IDR graph ID. |
| `identifiers[]` | array<object> | yes | Identifier values to queue for reprocessing, for example [{"identifier":"email","value":"a@b.com"}]. |
| `block` | boolean | no | Whether to block until reprocessing completes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `requestId` | string | IDR reprocessing request ID. |

## Native endpoint

Through the native Hightouch API, this operation is `POST /idr/{graphId}/queue-for-reprocessing` (base URL `https://api.hightouch.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/queue-idr-identifiers-for-reprocessing.md) for the provider-specific parameters and requirements.

