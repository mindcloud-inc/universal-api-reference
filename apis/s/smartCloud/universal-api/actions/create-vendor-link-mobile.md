# 2Smart Cloud: Link vendor account to mobile



```
POST https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-vendor-link-mobile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-vendor-link-mobile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "token": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-vendor-link-mobile', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "token": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `token` | string | yes | JWT token from email to link account |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar_url": "https://example.com",
      "category": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "is_blocked": true,
      "login": "string",
      "mqttCredentials": {},
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar_url` | string |  |
| `category` | string |  |
| `created` | date |  |
| `id` | number |  |
| `is_blocked` | boolean |  |
| `login` | string |  |
| `mqttCredentials` | object |  |
| `updated` | date |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `POST /vendor/link-mobile` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vendor-link-mobile.md) for the provider-specific parameters and requirements.

