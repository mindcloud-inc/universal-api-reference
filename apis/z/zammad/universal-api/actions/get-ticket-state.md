# Zammad: Get Ticket State

Retrieves a ticket state from Zammad.

```
GET https://connect.mindcloud.co/v1/universal/zammad/latest/actions/get-ticket-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zammad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zammad/latest/actions/get-ticket-state?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zammad/latest/actions/get-ticket-state?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Ticket state identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "defaultCreate": true,
      "defaultFollowUp": true,
      "id": 1,
      "ignoreEscalation": true,
      "name": "Ava Chen",
      "nextStateId": 1,
      "stateTypeId": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `createdAt` | date |  |
| `defaultCreate` | boolean |  |
| `defaultFollowUp` | boolean |  |
| `id` | number |  |
| `ignoreEscalation` | boolean |  |
| `name` | string |  |
| `nextStateId` | number |  |
| `stateTypeId` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Zammad API, this operation is `GET /ticket_states/:id` (base URL `{{credentials.baseUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket-state.md) for the provider-specific parameters and requirements.

