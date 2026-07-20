# Bento Now: Import Subscribers

Imports subscribers into Bento Now without triggering automations.

```
PUT https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/import-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bento Now `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/import-subscribers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscribers[].email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/import-subscribers', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscribers[].email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscribers[].email` | string | yes |  |

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

Through the native Bento Now API, this operation is `POST /v1/batch/subscribers` (base URL `https://app.bentonow.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-subscribers.md) for the provider-specific parameters and requirements.

