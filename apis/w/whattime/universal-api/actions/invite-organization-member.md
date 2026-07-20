# Whattime: Invite Organization Member



```
POST https://connect.mindcloud.co/v1/universal/whattime/latest/actions/invite-organization-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whattime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whattime/latest/actions/invite-organization-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whattime/latest/actions/invite-organization-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | 이메일 |
| `role` | string | no | 권한 * `owner` : 최고 관리자 * `admin` : 관리자 * `user` : 사용자 |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approve": true,
      "code": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "role": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "uri": "string",
      "user": {
        "code": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "name": "Ava Chen",
        "organization": {
          "code": "string",
          "created_at": "2026-05-07T12:00:00.000Z",
          "name": "Ava Chen",
          "updated_at": "2026-05-07T12:00:00.000Z",
          "uri": "string"
        },
        "role": "string",
        "slug": "string",
        "time_zone": "string",
        "updated_at": "2026-05-07T12:00:00.000Z",
        "uri": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approve` | boolean |  |
| `code` | string |  |
| `created_at` | date |  |
| `role` | string |  |
| `updated_at` | date |  |
| `uri` | string |  |
| `user` | object |  |
| `user.code` | string |  |
| `user.created_at` | date |  |
| `user.email` | string |  |
| `user.name` | string |  |
| `user.organization` | object |  |
| `user.organization.code` | string |  |
| `user.organization.created_at` | date |  |
| `user.organization.name` | string |  |
| `user.organization.updated_at` | date |  |
| `user.organization.uri` | string |  |
| `user.role` | string |  |
| `user.slug` | string |  |
| `user.time_zone` | string |  |
| `user.updated_at` | date |  |
| `user.uri` | string |  |

## Native endpoint

Through the native Whattime API, this operation is `POST /organization_members` (base URL `https://api.whattime.co.kr/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-organization-member.md) for the provider-specific parameters and requirements.

