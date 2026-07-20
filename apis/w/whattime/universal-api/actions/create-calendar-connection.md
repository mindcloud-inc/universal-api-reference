# Whattime: Create Calendar Connection



```
POST https://connect.mindcloud.co/v1/universal/whattime/latest/actions/create-calendar-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whattime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whattime/latest/actions/create-calendar-connection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "kind": "string",
  "email": "ava@example.com",
  "password": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whattime/latest/actions/create-calendar-connection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "kind": "string",
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
| `user` | string | no | User uri |
| `kind` | string | yes |  |
| `email` | string | yes | 아이디(이메일) |
| `password` | string | yes | 비밀번호 |

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

Through the native Whattime API, this operation is `POST /connects` (base URL `https://api.whattime.co.kr/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-calendar-connection.md) for the provider-specific parameters and requirements.

