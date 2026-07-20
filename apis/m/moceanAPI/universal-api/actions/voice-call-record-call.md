# Mocean API: Voice Call Record Call



```
POST https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/voice-call-record-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mocean API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/voice-call-record-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recipient": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/voice-call-record-call', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recipient": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recipient` | string | yes | Phone number to call, including country code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calls": [
        {
          "id": "string",
          "recipient": "string",
          "status": "string"
        }
      ],
      "error": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calls[].id` | string |  |
| `calls[].recipient` | string |  |
| `calls[].status` | string |  |
| `error` | string |  |

## Native endpoint

Through the native Mocean API API, this operation is `POST /rest/2/voice/dial?mocean-resp-format=json&mocean-command=%5B%7B%22action%22%3A%22record%22%7D%2C%7B%22action%22%3A%22say%22%2C%22text%22%3A%22This%20call%20is%20being%20recorded%22%2C%22language%22%3A%22en-US%22%7D%5D` (base URL `https://rest.moceanapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/voice-call-record-call.md) for the provider-specific parameters and requirements.

