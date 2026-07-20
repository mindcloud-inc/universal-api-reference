# Bento Now: Create Events

Tracks user activity in Bento Now.

```
POST https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/create-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bento Now `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/create-events" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "events[].email": "ava@example.com",
  "events[].type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/create-events', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "events[].email": "ava@example.com",
    "events[].type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `events[].email` | string | yes |  |
| `events[].type` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "failed": 1,
      "results": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `failed` | number |  |
| `results` | number |  |

## Native endpoint

Through the native Bento Now API, this operation is `POST /v1/batch/events` (base URL `https://app.bentonow.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-events.md) for the provider-specific parameters and requirements.

