# Virtually: Create Member

Creates a new member in Virtually.

```
POST https://connect.mindcloud.co/v1/universal/virtually/latest/actions/create-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Virtually `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/virtually/latest/actions/create-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "email": "ava@example.com",
  "tagIds[]": [
    "string"
  ],
  "role": "string",
  "properties": {},
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/virtually/latest/actions/create-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "email": "ava@example.com",
    "tagIds[]": ["string"],
    "role": "string",
    "properties": {},
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The member name. |
| `email` | string | yes | The member email address. |
| `tagIds[]` | array<string> | yes | The tag IDs to assign to the member. |
| `role` | string | yes | The member role. |
| `properties` | object | yes | Additional member properties. |
| `status` | string | yes | The member status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "memberId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `memberId` | string | The created member ID. |

## Native endpoint

Through the native Virtually API, this operation is `POST /api/v2/orgs/:orgId/members` (base URL `https://app.tryvirtually.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-member.md) for the provider-specific parameters and requirements.

