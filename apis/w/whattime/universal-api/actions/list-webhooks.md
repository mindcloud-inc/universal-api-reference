# Whattime: List Webhooks



```
GET https://connect.mindcloud.co/v1/universal/whattime/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whattime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whattime/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whattime/latest/actions/list-webhooks?${params}`, {
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
| `organization` | string | no | Organization uri (User 모델에 organization.uri 를 참고해 주세요) |
| `user` | string | no | User uri (User 모델에 uri 를 확인해 주세요) |
| `kind` | string | no | 콜벡 종류 |
| `per` | number | no | 가져올 개수 |
| `pageToken` | string | no | 가져올 다음페이지 토큰 |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callback_url": "https://example.com",
      "code": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "kind": "string",
      "organization": {
        "code": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "updated_at": "2026-05-07T12:00:00.000Z",
        "uri": "string"
      },
      "provider": "string",
      "scope": "string",
      "status": "string",
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
| `callback_url` | string |  |
| `code` | string |  |
| `created_at` | date |  |
| `kind` | string |  |
| `organization` | object |  |
| `organization.code` | string |  |
| `organization.created_at` | date |  |
| `organization.name` | string |  |
| `organization.updated_at` | date |  |
| `organization.uri` | string |  |
| `provider` | string |  |
| `scope` | string |  |
| `status` | string |  |
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

Through the native Whattime API, this operation is `GET /webhooks` (base URL `https://api.whattime.co.kr/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

