# Hightouch: Update Event Contract

Updates an event contract in Hightouch.

```
PUT https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/update-event-contract
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hightouch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/update-event-contract" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contractId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/update-event-contract', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contractId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contractId` | string | yes | The event contract ID. |
| `description` | string | no | The event contract description. |
| `name` | string | no | The event contract name. |
| `onUndeclaredSchema` | string | no | Behavior for events not defined in the contract. |
| `slug` | string | no | The event contract slug. |
| `events[]` | array<object> | no | Event definitions in the contract. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "events": [
        {}
      ],
      "name": "Ava Chen",
      "onUndeclaredSchema": "string",
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Contract description. |
| `events` | array<object> | Contract event definitions. |
| `name` | string | Contract name. |
| `onUndeclaredSchema` | string | Behavior for undeclared event schemas. |
| `slug` | string | Contract slug. |

## Native endpoint

Through the native Hightouch API, this operation is `PATCH /events/contracts/{contractId}` (base URL `https://api.hightouch.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-event-contract.md) for the provider-specific parameters and requirements.

