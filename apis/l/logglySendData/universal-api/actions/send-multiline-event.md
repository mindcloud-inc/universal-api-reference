# Loggly (Send Data): Send Multiline Event

Creates a multiline log event in Loggly.

```
POST https://connect.mindcloud.co/v1/universal/logglySendData/latest/actions/send-multiline-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loggly (Send Data) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/logglySendData/latest/actions/send-multiline-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerToken": "123e4567-e89b-12d3-a456-426614174000",
  "tagPath": "app/server",
  "message": "Error: stack trace line 1\n    at service.js:10\n    at handler.js:42"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logglySendData/latest/actions/send-multiline-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerToken": "123e4567-e89b-12d3-a456-426614174000",
    "tagPath": "app/server",
    "message": "Error: stack trace line 1\n    at service.js:10\n    at handler.js:42"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerToken` | string | yes | Example: `123e4567-e89b-12d3-a456-426614174000`. |
| `tagPath` | string | yes | Example: `app/server`. |
| `message` | string | yes | Example: `Error: stack trace line 1     at service.js:10     at handler.js:42`. |

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
| `response` | string | Loggly ingestion acknowledgement message. |

## Native endpoint

Through the native Loggly (Send Data) API, this operation is `POST /inputs/:customerToken/tag/:tagPath/` (base URL `https://logs-01.loggly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-multiline-event.md) for the provider-specific parameters and requirements.

