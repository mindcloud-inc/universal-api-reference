# Neon: Update role for organization member

Updates a role for organization member in Neon.

```
PUT https://connect.mindcloud.co/v1/universal/neon/latest/actions/update-organization-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/neon/latest/actions/update-organization-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "org_id": "string",
  "member_id": "string",
  "role": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neon/latest/actions/update-organization-member', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "org_id": "string",
    "member_id": "string",
    "role": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `org_id` | string | yes | Neon API parameter org_id |
| `member_id` | string | yes | Neon API parameter member_id |
| `role` | list | yes | Neon API parameter role One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "joined_at": "2026-05-07T12:00:00.000Z",
      "org_id": "string",
      "role": [
        "string"
      ],
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `joined_at` | date |  |
| `org_id` | string |  |
| `role` | array |  |
| `user_id` | string |  |

## Native endpoint

Through the native Neon API, this operation is `PATCH /organizations/:org_id/members/:member_id` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-organization-member.md) for the provider-specific parameters and requirements.

