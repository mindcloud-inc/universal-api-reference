# Whattime: List Organization Members



```
GET https://connect.mindcloud.co/v1/universal/whattime/latest/actions/list-organization-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whattime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whattime/latest/actions/list-organization-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whattime/latest/actions/list-organization-members?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `user` | string | no | User uri (User 모델에 uri 를 확인해 주세요) |
| `email` | string | no | 멤버 이메일 |
| `approve` | boolean | no | 승인 여부 |
| `sort` | string | no | 정렬 필드 `id` : 생성일, `role` : 권한 , `email` : 이메일 |
| `order` | string | no | 오름,내림 차순 |
| `per` | number | no | 가져올 개수 |
| `pageToken` | string | no | 가져올 다음페이지 토큰 |

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

Through the native Whattime API, this operation is `GET /organization_members` (base URL `https://api.whattime.co.kr/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organization-members.md) for the provider-specific parameters and requirements.

