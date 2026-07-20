# Trint: Start New Realtime Transcript

Starts a new realtime transcript in Trint.

```
PUT https://connect.mindcloud.co/v1/universal/trint/latest/actions/start-new-realtime-transcript
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/trint/latest/actions/start-new-realtime-transcript" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trint/latest/actions/start-new-realtime-transcript', {
  method: 'PUT',
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "trintId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Realtime transcript status after start was requested. |
| `trintId` | string | Realtime transcript identifier. |

## Native endpoint

Through the native Trint API, this operation is `PUT /transcripts/realtime/` (base URL `https://api.trint.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-new-realtime-transcript.md) for the provider-specific parameters and requirements.

