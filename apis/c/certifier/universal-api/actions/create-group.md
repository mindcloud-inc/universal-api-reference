# Certifier: Create Group

Creates a new group in Certifier.

```
POST https://connect.mindcloud.co/v1/universal/certifier/latest/actions/create-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Certifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/certifier/latest/actions/create-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/certifier/latest/actions/create-group', {
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
| `name` | string | yes |  |
| `certificate_design_id` | string | no |  |
| `badge_design_id` | string | no |  |
| `learning_event_url` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "badgeDesignId": "string",
      "certificateDesignId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "learningEventUrl": "https://example.com",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `badgeDesignId` | string |  |
| `certificateDesignId` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `learningEventUrl` | string |  |
| `name` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Certifier API, this operation is `POST /groups` (base URL `https://api.certifier.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-group.md) for the provider-specific parameters and requirements.

