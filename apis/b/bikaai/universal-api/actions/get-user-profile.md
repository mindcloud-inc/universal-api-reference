# Bika.ai: Get User Profile

Retrieves your Bika.ai user profile.

```
GET https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/get-user-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bika.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/get-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/get-user-profile?${params}`, {
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
      "avatar": {
        "color": "string",
        "type": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "metadata": {
        "isChinaUser": true
      },
      "name": "Ava Chen",
      "settings": {
        "locale": "string"
      },
      "status": "string",
      "timeZone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | object |  |
| `avatar.color` | string |  |
| `avatar.type` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `metadata.isChinaUser` | boolean |  |
| `name` | string |  |
| `settings` | object |  |
| `settings.locale` | string |  |
| `status` | string |  |
| `timeZone` | string |  |

## Native endpoint

Through the native Bika.ai API, this operation is `GET /user/profile` (base URL `https://bika.ai/api/openapi/bika/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-profile.md) for the provider-specific parameters and requirements.

