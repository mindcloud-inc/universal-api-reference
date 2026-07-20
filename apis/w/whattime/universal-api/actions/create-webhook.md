# Whattime: Create Webhook



```
POST https://connect.mindcloud.co/v1/universal/whattime/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whattime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whattime/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "kind": "string",
  "callbackUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whattime/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "kind": "string",
    "callbackUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `kind` | string | yes | 콜백 종류 * `schedule_created` - 예약 생성 * `schedule_canceled` - 예약 취소 * `user_changed` - 유저 정보 변경 * `user_withdraw` - 유저 탈퇴 |
| `organization` | string | no | Organization uri |
| `user` | string | no | User uri |
| `callbackUrl` | string | yes | 콜백 받을 주소 |
| `scope` | string | no | 콜백 종류 * `user` - 특정 유저 * `organization` - 조직 전체 |
| `signingKey` | string | no | 보안을 위한 사이닝 키 <br> `WhatTime-Webhook-Signature` : `t={timestamp},v1={signing_key}` 가 헤더값에 추가됩니다. |

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

Through the native Whattime API, this operation is `POST /webhooks` (base URL `https://api.whattime.co.kr/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

