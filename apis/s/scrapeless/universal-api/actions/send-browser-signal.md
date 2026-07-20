# Scrapeless: Send Browser Signal

Creates a browser signal in Scrapeless.

```
POST https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/send-browser-signal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapeless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/send-browser-signal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string",
  "event": "string",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/send-browser-signal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string",
    "event": "string",
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | session task id |
| `xApiToken` | string | no | API Key |
| `event` | string | yes | Event channel name (1-256 characters) |
| `data` | object | yes | Event data payload |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | number |  |

## Native endpoint

Through the native Scrapeless API, this operation is `POST /browser/:taskId/signal/send` (base URL `https://api.scrapeless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-browser-signal.md) for the provider-specific parameters and requirements.

