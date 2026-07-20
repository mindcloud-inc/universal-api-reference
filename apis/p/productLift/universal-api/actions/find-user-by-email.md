# ProductLift: Find User By Email



```
GET https://connect.mindcloud.co/v1/universal/productLift/latest/actions/find-user-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProductLift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productLift/latest/actions/find-user-by-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productLift/latest/actions/find-user-by-email?${params}`, {
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
      "databaseId": 1,
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `databaseId` | number |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native ProductLift API, this operation is `GET /users/find_by_email` (base URL `https://mindcloud.productlift.dev/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-user-by-email.md) for the provider-specific parameters and requirements.

