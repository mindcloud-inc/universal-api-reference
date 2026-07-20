# Supernotes: Get Known Owner Profiles

Retrieves known card owner profiles from Supernotes.

```
GET https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-known-owner-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supernotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-known-owner-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-known-owner-profiles?${params}`, {
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
      "bio": "string",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "photo": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bio` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `photo` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Supernotes API, this operation is `GET /profiles/known` (base URL `https://api.supernotes.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-known-owner-profiles.md) for the provider-specific parameters and requirements.

