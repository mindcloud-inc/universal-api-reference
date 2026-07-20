# Habitica: Get User

Retrieves the current user from Habitica.

```
GET https://connect.mindcloud.co/v1/universal/habitica/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Habitica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/habitica/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/habitica/latest/actions/get-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "appVersion": "string",
      "id": "string",
      "items": {},
      "notifications": [
        {}
      ],
      "preferences": {},
      "profile": {},
      "stats": {},
      "tags": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appVersion` | string |  |
| `id` | string |  |
| `items` | object |  |
| `notifications` | array<object> |  |
| `preferences` | object |  |
| `profile` | object |  |
| `stats` | object |  |
| `tags` | array<object> |  |

## Native endpoint

Through the native Habitica API, this operation is `GET /user` (base URL `https://habitica.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

