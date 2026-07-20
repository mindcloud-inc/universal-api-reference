# Hightouch: Create Event Contract

Creates a new event contract in Hightouch.

```
POST https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/create-event-contract
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hightouch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/create-event-contract" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/create-event-contract', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | The event contract description. |
| `name` | string | yes | The event contract name. |
| `onUndeclaredSchema` | string | no | Behavior for events not defined in the contract. |
| `slug` | string | no | The event contract slug. If omitted, Hightouch generates one. |
| `events[]` | array<object> | no | Event definitions in the contract. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "events": [
        {}
      ],
      "eventSources": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "onUndeclaredSchema": "string",
      "slug": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `description` | string | Contract description. |
| `events` | array<object> | Contract event definitions. |
| `eventSources` | array<object> | Linked event sources. |
| `id` | string | Contract ID. |
| `name` | string | Contract name. |
| `onUndeclaredSchema` | string | Behavior for undeclared event schemas. |
| `slug` | string | Contract slug. |
| `updatedAt` | date | Last update timestamp. |
| `workspaceId` | number | Workspace ID. |

## Native endpoint

Through the native Hightouch API, this operation is `POST /events/contracts` (base URL `https://api.hightouch.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event-contract.md) for the provider-specific parameters and requirements.

