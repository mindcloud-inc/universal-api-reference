# Whattime: List Calendar Connections



```
GET https://connect.mindcloud.co/v1/universal/whattime/latest/actions/list-calendar-connections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whattime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whattime/latest/actions/list-calendar-connections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whattime/latest/actions/list-calendar-connections?${params}`, {
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
| `per` | number | no | 가져올 개수 |
| `pageToken` | string | no | 가져올 다음페이지 토큰 |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "error": true,
      "kind": "string",
      "uid": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `email` | string |  |
| `error` | boolean |  |
| `kind` | string |  |
| `uid` | string |  |
| `updated_at` | date |  |
| `uri` | string |  |

## Native endpoint

Through the native Whattime API, this operation is `GET /connects` (base URL `https://api.whattime.co.kr/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-calendar-connections.md) for the provider-specific parameters and requirements.

