# Loggly (Send Data): Send Plaintext Event

Creates a plain-text log event in Loggly.

```
POST https://connect.mindcloud.co/v1/universal/logglySendData/latest/actions/send-plaintext-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loggly (Send Data) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/logglySendData/latest/actions/send-plaintext-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerToken": "123e4567-e89b-12d3-a456-426614174000",
  "tagPath": "app/server",
  "message": "user login succeeded"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logglySendData/latest/actions/send-plaintext-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerToken": "123e4567-e89b-12d3-a456-426614174000",
    "tagPath": "app/server",
    "message": "user login succeeded"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerToken` | string | yes | Loggly customer token used in the ingestion URL path. Example: `123e4567-e89b-12d3-a456-426614174000`. |
| `tagPath` | string | yes | One tag or a slash-delimited tag path to attach to the event. Example: `app/server`. |
| `message` | string | yes | Plain-text message content to send to Loggly. Example: `user login succeeded`. |

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

Through the native Loggly (Send Data) API, this operation is `POST /inputs/:customerToken/tag/:tagPath/` (base URL `https://logs-01.loggly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-plaintext-event.md) for the provider-specific parameters and requirements.

