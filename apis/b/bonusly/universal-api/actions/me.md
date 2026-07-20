# Bonusly: Me

Retrieves the authenticated user from Bonusly.

```
GET https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/me
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bonusly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/me?${params}`, {
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
      "createdAt": "string",
      "displayName": "Ava Chen",
      "earningBalance": 1,
      "email": "ava@example.com",
      "givingBalance": 1,
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `displayName` | string |  |
| `earningBalance` | number |  |
| `email` | string |  |
| `givingBalance` | number |  |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Bonusly API, this operation is `GET /users/me` (base URL `https://bonus.ly/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/me.md) for the provider-specific parameters and requirements.

