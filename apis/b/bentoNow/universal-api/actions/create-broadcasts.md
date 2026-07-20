# Bento Now: Create Broadcasts

Creates a broadcast campaign in Bento Now.

```
POST https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/create-broadcasts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bento Now `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/create-broadcasts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "broadcasts[].content": "string",
  "broadcasts[].name": "Ava Chen",
  "broadcasts[].subject": "string",
  "broadcasts[].type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/create-broadcasts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "broadcasts[].content": "string",
    "broadcasts[].name": "Ava Chen",
    "broadcasts[].subject": "string",
    "broadcasts[].type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `broadcasts[].content` | string | yes |  |
| `broadcasts[].name` | string | yes |  |
| `broadcasts[].subject` | string | yes |  |
| `broadcasts[].type` | string | yes |  |

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

Through the native Bento Now API, this operation is `POST /v1/batch/broadcasts` (base URL `https://app.bentonow.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-broadcasts.md) for the provider-specific parameters and requirements.

