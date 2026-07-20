# Uspacy: Get Self Profile

Retrieves the authenticated user profile from Uspacy.

```
GET https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/get-self-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uspacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/get-self-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/get-self-profile?${params}`, {
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
      "active": true,
      "firstName": "Ava",
      "id": 1,
      "isOnline": true,
      "lastName": "Chen",
      "lastSeenAt": "2026-05-07T12:00:00.000Z",
      "registered": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `firstName` | string |  |
| `id` | number |  |
| `isOnline` | boolean |  |
| `lastName` | string |  |
| `lastSeenAt` | date |  |
| `registered` | boolean |  |

## Native endpoint

Through the native Uspacy API, this operation is `GET /company/v1/users/me` (base URL `https://{{credentials.site}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-self-profile.md) for the provider-specific parameters and requirements.

