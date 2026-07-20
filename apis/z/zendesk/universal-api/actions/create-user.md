# Zendesk: Create User

Creates a new user in Zendesk.

```
POST https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zendesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "user.name": "Jane Doe"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "user.name": "Jane Doe"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `user.name` | string | yes | Name for the new user. Default: `Jane Doe`. Example: `Jane Doe`. |
| `user.email` | string | no | Email for the new user. Default: `jane.doe@example.com`. Example: `jane.doe@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "organizationId": 1,
      "role": "string",
      "tags": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "verified": true
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
| `email` | string |  |
| `id` | number |  |
| `name` | string |  |
| `organizationId` | number |  |
| `role` | string |  |
| `tags[]` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `verified` | boolean |  |

## Native endpoint

Through the native Zendesk API, this operation is `POST /users.json` (base URL `https://{{credentials.subdomain}}.zendesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

