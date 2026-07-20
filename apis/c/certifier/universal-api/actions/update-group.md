# Certifier: Update Group

Updates an existing group in Certifier.

```
PUT https://connect.mindcloud.co/v1/universal/certifier/latest/actions/update-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Certifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/certifier/latest/actions/update-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/certifier/latest/actions/update-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `name` | string | no |  |
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

Through the native Certifier API, this operation is `PATCH /groups/:id` (base URL `https://api.certifier.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-group.md) for the provider-specific parameters and requirements.

