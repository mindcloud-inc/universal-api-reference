# LinkedIn: Get User Info

Retrieves the authenticated user's profile from LinkedIn.

```
GET https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/get-user-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkedIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/get-user-info?${params}`, {
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
      "email": "ava@example.com",
      "emailVerified": true,
      "familyName": "Ava Chen",
      "givenName": "Ava Chen",
      "locale": {
        "country": "string",
        "language": "string"
      },
      "name": "Ava Chen",
      "sub": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `emailVerified` | boolean |  |
| `familyName` | string |  |
| `givenName` | string |  |
| `locale` | object |  |
| `locale.country` | string |  |
| `locale.language` | string |  |
| `name` | string |  |
| `sub` | string |  |

## Native endpoint

Through the native LinkedIn API, this operation is `GET /v2/userinfo` (base URL `https://api.linkedin.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-info.md) for the provider-specific parameters and requirements.

