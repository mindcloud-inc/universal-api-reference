# Apilio: Evaluate Logicblock



```
PUT https://connect.mindcloud.co/v1/universal/apilio/latest/actions/evaluate-logicblock
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apilio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/apilio/latest/actions/evaluate-logicblock" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "a40f21df-7707-4898-9688-69bf1f8dd184"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apilio/latest/actions/evaluate-logicblock', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuid": "a40f21df-7707-4898-9688-69bf1f8dd184"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uuid` | string | yes | The UUID of the logicblock to evaluate. Default: `a40f21df-7707-4898-9688-69bf1f8dd184`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "evaluate": true,
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `evaluate` | boolean |  |
| `name` | string |  |
| `updatedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Apilio API, this operation is `POST /api/v1/logicblocks/{{uuid}}/evaluate` (base URL `https://api.apilio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/evaluate-logicblock.md) for the provider-specific parameters and requirements.

