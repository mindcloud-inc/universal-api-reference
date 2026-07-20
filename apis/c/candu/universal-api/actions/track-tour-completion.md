# Candu: Track Tour Completion

Tracks a tour completion event in Candu.

```
POST https://connect.mindcloud.co/v1/universal/candu/latest/actions/track-tour-completion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Candu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/candu/latest/actions/track-tour-completion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string",
  "properties": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/candu/latest/actions/track-tour-completion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string",
    "properties": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | The user ID the SDK event belongs to. |
| `properties` | object | yes | Required event-specific properties for the Candu tour completion event. |
| `timestamp` | date | no | Optional event timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | True when Candu accepts the event webhook request. |

## Native endpoint

Through the native Candu API, this operation is `POST /eventWebhook` (base URL `https://api.candu.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-tour-completion.md) for the provider-specific parameters and requirements.

