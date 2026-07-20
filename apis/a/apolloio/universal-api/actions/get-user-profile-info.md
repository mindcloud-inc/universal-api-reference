# Apollo: Get User Profile Info

Retrieves the authorized user profile from Apollo.

```
GET https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/get-user-profile-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apollo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/get-user-profile-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/get-user-profile-info?${params}`, {
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
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "teamId": "string",
      "title": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `teamId` | string |  |
| `title` | object |  |

## Native endpoint

Through the native Apollo API, this operation is `GET v1/users/api_profile` (base URL `https://app.apollo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-profile-info.md) for the provider-specific parameters and requirements.

