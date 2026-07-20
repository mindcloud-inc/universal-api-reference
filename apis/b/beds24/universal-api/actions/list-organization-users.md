# Beds24: List Organization Users

Retrieves organization users from Beds24.

```
GET https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-organization-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beds24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-organization-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-organization-users?${params}`, {
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
      "masterId": 1,
      "ownerId": 1,
      "properties": [
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
| `email` | string |  |
| `masterId` | number |  |
| `ownerId` | number |  |
| `properties` | array<object> |  |

## Native endpoint

Through the native Beds24 API, this operation is `GET /organizations/users` (base URL `https://beds24.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organization-users.md) for the provider-specific parameters and requirements.

