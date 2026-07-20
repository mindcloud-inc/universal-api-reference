# MailerCheck: Create Verification List

Creates a verification list in MailerCheck.

```
POST https://connect.mindcloud.co/v1/universal/mailerCheck/latest/actions/create-verification-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerCheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailerCheck/latest/actions/create-verification-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "emails[]": [
    "ava@example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailerCheck/latest/actions/create-verification-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "emails[]": ["ava@example.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Verification list name. |
| `emails[]` | array<string> | yes | Email addresses to add to the verification list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "count": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "source": "string",
      "statistics": {},
      "status": {},
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `count` | number |  |
| `createdAt` | date |  |
| `id` | number |  |
| `name` | string |  |
| `source` | string |  |
| `statistics` | object |  |
| `status` | object |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `userId` | number |  |

## Native endpoint

Through the native MailerCheck API, this operation is `POST /lists` (base URL `https://app.mailercheck.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-verification-list.md) for the provider-specific parameters and requirements.

