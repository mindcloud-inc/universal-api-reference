# Locu: Create Session

Creates a new work session in Locu.

```
POST https://connect.mindcloud.co/v1/universal/locu/latest/actions/create-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Locu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/locu/latest/actions/create-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "createdAt": "2026-05-07T12:00:00.000Z",
  "finishedAt": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/locu/latest/actions/create-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "createdAt": "2026-05-07T12:00:00.000Z",
    "finishedAt": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createdAt` | date | yes |  |
| `finishedAt` | date | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "finishedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isManual": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `finishedAt` | date |  |
| `id` | string |  |
| `isManual` | boolean |  |

## Native endpoint

Through the native Locu API, this operation is `POST /sessions` (base URL `https://api.locu.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-session.md) for the provider-specific parameters and requirements.

