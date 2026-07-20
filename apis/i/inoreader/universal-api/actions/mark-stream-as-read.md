# Inoreader: Mark Stream As Read

Marks an Inoreader stream as read.

```
PUT https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/mark-stream-as-read
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Inoreader `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/mark-stream-as-read" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "streamId": "string",
  "timestamp": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/mark-stream-as-read', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "streamId": "string",
    "timestamp": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `streamId` | string | yes | Stream ID to mark as read. |
| `timestamp` | number | yes | Unix timestamp in seconds or microseconds from the last displayed fetch. |

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
| `response` | string | Provider acknowledgement returned by Inoreader for the mark-all-as-read mutation. |

## Native endpoint

Through the native Inoreader API, this operation is `POST /mark-all-as-read` (base URL `https://www.inoreader.com/reader/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-stream-as-read.md) for the provider-specific parameters and requirements.

