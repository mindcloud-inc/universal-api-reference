# Loggly (Send Data): Send Tracking Pixel Event

Creates a tracking-pixel log event in Loggly.

```
POST https://connect.mindcloud.co/v1/universal/logglySendData/latest/actions/send-tracking-pixel-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loggly (Send Data) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/logglySendData/latest/actions/send-tracking-pixel-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerToken": "123e4567-e89b-12d3-a456-426614174000",
  "message": "hello world!"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logglySendData/latest/actions/send-tracking-pixel-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerToken": "123e4567-e89b-12d3-a456-426614174000",
    "message": "hello world!"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerToken` | string | yes | Example: `123e4567-e89b-12d3-a456-426614174000`. |
| `message` | string | yes | Example: `hello world!`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Binary 1x1 GIF payload returned by the Loggly tracking pixel endpoint. |

## Native endpoint

Through the native Loggly (Send Data) API, this operation is `GET /inputs/:customerToken.gif` (base URL `https://logs-01.loggly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-tracking-pixel-event.md) for the provider-specific parameters and requirements.

