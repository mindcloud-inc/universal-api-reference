# Sonderplan: Get Users



```
GET https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sonderplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-users?${params}`, {
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
      "firstName": "Ava",
      "groupId": 1,
      "id": 1,
      "lastName": "Chen",
      "locale": "string",
      "primaryEmail": "ava@example.com",
      "timezone": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `firstName` | string |  |
| `groupId` | number |  |
| `id` | number |  |
| `lastName` | string |  |
| `locale` | string |  |
| `primaryEmail` | string |  |
| `timezone` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Sonderplan API, this operation is `GET /user` (base URL `https://api.sonderplan.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-users.md) for the provider-specific parameters and requirements.

