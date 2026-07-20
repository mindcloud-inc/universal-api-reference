# Mailcoach: Update Subscriber

Updates an existing subscriber in Mailcoach.

```
PUT https://connect.mindcloud.co/v1/universal/mailcoach/latest/actions/update-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailcoach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailcoach/latest/actions/update-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailcoach/latest/actions/update-subscriber', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "uuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appendTags` | boolean | no | Append tags instead of replacing them. |
| `email` | string | yes | The subscriber email address. |
| `extraAttributes` | object | no | Additional subscriber attributes as an object. |
| `firstName` | string | no | The subscriber first name. |
| `lastName` | string | no | The subscriber last name. |
| `tags[]` | array<string> | no | Tags to sync or append to the subscriber. |
| `uuid` | string | yes | The UUID of the subscriber to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "emailListUuid": "ava@example.com",
      "extraAttributes": {},
      "firstName": "Ava",
      "lastName": "Chen",
      "subscribedAt": "2026-05-07T12:00:00.000Z",
      "tags": [
        "string"
      ],
      "unsubscribedAt": "2026-05-07T12:00:00.000Z",
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
| `createdAt` | date |  |
| `email` | string |  |
| `emailListUuid` | string |  |
| `extraAttributes` | object |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `subscribedAt` | date |  |
| `tags` | array<string> |  |
| `unsubscribedAt` | date |  |
| `updatedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Mailcoach API, this operation is `PATCH /subscribers/:uuid` (base URL `https://mindcloud.mailcoach.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscriber.md) for the provider-specific parameters and requirements.

