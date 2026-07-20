# Moco: Get Profile



```
GET https://connect.mindcloud.co/v1/universal/moco/latest/actions/get-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moco/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moco/latest/actions/get-profile?${params}`, {
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
      "avatarUrl": {},
      "createdAt": "string",
      "email": "ava@example.com",
      "external": true,
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": 1,
      "lastName": "Chen",
      "unit": {
        "id": 1,
        "name": "Ava Chen"
      },
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `avatarUrl` | object |  |
| `createdAt` | string |  |
| `email` | string |  |
| `external` | boolean |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `unit` | object |  |
| `unit.id` | number |  |
| `unit.name` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Moco API, this operation is `GET /profile` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-profile.md) for the provider-specific parameters and requirements.

