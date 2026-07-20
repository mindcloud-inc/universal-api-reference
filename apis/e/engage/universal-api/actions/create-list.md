# Engage: Create List

Creates a new list in Engage.

```
POST https://connect.mindcloud.co/v1/universal/engage/latest/actions/create-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Engage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/engage/latest/actions/create-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/engage/latest/actions/create-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `doubleOptin` | boolean | no | Set to true to send a confirmation email to subscribers. |
| `redirectUrl` | string | no | URL to redirect users to after subscription. |
| `title` | string | yes | List title. |
| `description` | string | no | List description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "broadcastCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "doubleOptin": true,
      "id": "string",
      "redirectUrl": "https://example.com",
      "subscriberCount": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `broadcastCount` | number |  |
| `createdAt` | date |  |
| `description` | string |  |
| `doubleOptin` | boolean |  |
| `id` | string |  |
| `redirectUrl` | string |  |
| `subscriberCount` | number |  |
| `title` | string |  |

## Native endpoint

Through the native Engage API, this operation is `POST /lists` (base URL `https://api.engage.so/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-list.md) for the provider-specific parameters and requirements.

