# 2Smart Cloud: Show share-link



```
GET https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-share-v1-short-link-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-share-v1-short-link-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-share-v1-short-link-by-id?${params}`, {
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
| `id` | string | yes | ID of short link |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active_from": "2026-05-07T12:00:00.000Z",
      "active_to": "2026-05-07T12:00:00.000Z",
      "created": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "is_active": true,
      "link": "https://example.com",
      "name": "Ava Chen",
      "token": {},
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active_from` | date | Activation start |
| `active_to` | date | Activation end |
| `created` | date | Creation timestamp |
| `id` | number | Share link identifier |
| `is_active` | boolean | Whether the link is active |
| `link` | string | Share link URL |
| `name` | string | Share link name |
| `token` | object | MQTT token payload |
| `updated` | date | Update timestamp |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `GET /share/v1/short-link/{id}` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-share-v1-short-link-by-id.md) for the provider-specific parameters and requirements.

