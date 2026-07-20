# Eventzilla: List Users

Retrieves users from Eventzilla.

```
GET https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventzilla `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/list-users?${params}`, {
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
      "addressCountry": "string",
      "addressLine1": "string",
      "addressLine2": "string",
      "addressLocality": "string",
      "addressRegion": "string",
      "avatarUrl": "https://example.com",
      "company": "string",
      "email": "ava@example.com",
      "facebookId": "string",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "lastSeen": "string",
      "phonePrimary": "string",
      "timezone": "string",
      "twitterId": "string",
      "username": "Ava Chen",
      "userType": "string",
      "website": "string",
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressCountry` | string |  |
| `addressLine1` | string |  |
| `addressLine2` | string |  |
| `addressLocality` | string |  |
| `addressRegion` | string |  |
| `avatarUrl` | string |  |
| `company` | string |  |
| `email` | string |  |
| `facebookId` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `lastSeen` | string |  |
| `phonePrimary` | string |  |
| `timezone` | string |  |
| `twitterId` | string |  |
| `username` | string |  |
| `userType` | string |  |
| `website` | string |  |
| `zipCode` | string |  |

## Native endpoint

Through the native Eventzilla API, this operation is `GET /users` (base URL `https://www.eventzillaapi.net/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

