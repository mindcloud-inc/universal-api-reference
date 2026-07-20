# Loggly (Send Data): Send Bulk Events

Creates bulk log events in Loggly.

```
POST https://connect.mindcloud.co/v1/universal/logglySendData/latest/actions/send-bulk-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loggly (Send Data) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/logglySendData/latest/actions/send-bulk-events" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerToken": "123e4567-e89b-12d3-a456-426614174000",
  "tagPath": "app/server",
  "events": "first event line\\nsecond event line"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logglySendData/latest/actions/send-bulk-events', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerToken": "123e4567-e89b-12d3-a456-426614174000",
    "tagPath": "app/server",
    "events": "first event line\\nsecond event line"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerToken` | string | yes | Loggly customer token used in the ingestion URL path. Example: `123e4567-e89b-12d3-a456-426614174000`. |
| `tagPath` | string | yes | One tag or a slash-delimited tag path to attach to all bulk events. Example: `app/server`. |
| `events` | string | yes | Newline-delimited bulk event payload. Example: `first event line\nsecond event line`. |

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

Through the native Loggly (Send Data) API, this operation is `POST /bulk/:customerToken/tag/:tagPath/` (base URL `https://logs-01.loggly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-bulk-events.md) for the provider-specific parameters and requirements.

