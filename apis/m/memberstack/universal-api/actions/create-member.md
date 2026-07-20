# Memberstack: Create Member



```
POST https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/create-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Memberstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/create-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "password": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/create-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "password": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Member email address for the new member. |
| `password` | string | yes | Password for the new member (minimum 8 characters). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auth": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFields": {},
      "id": "string",
      "lastLogin": "2026-05-07T12:00:00.000Z",
      "loginRedirect": "string",
      "metaData": {},
      "permissions": [
        "string"
      ],
      "planConnections": [
        {}
      ],
      "profileImage": "string",
      "stripeCustomerId": "string",
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auth` | object |  |
| `createdAt` | date |  |
| `customFields` | object |  |
| `id` | string |  |
| `lastLogin` | date |  |
| `loginRedirect` | string |  |
| `metaData` | object |  |
| `permissions` | array<string> |  |
| `planConnections` | array<object> |  |
| `profileImage` | string |  |
| `stripeCustomerId` | string |  |
| `verified` | boolean |  |

## Native endpoint

Through the native Memberstack API, this operation is `POST /members` (base URL `https://admin.memberstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-member.md) for the provider-specific parameters and requirements.

