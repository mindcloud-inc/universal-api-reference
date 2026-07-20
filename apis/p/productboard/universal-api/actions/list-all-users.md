# Productboard: List All Users

Retrieves users from your Productboard workspace.

```
GET https://connect.mindcloud.co/v1/universal/productboard/latest/actions/list-all-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productboard/latest/actions/list-all-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productboard/latest/actions/list-all-users?${params}`, {
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
      "companyId": "string",
      "email": "ava@example.com",
      "externalId": "string",
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
| `companyId` | string | Associated Productboard company identifier. |
| `email` | string | User email address when available. |
| `externalId` | string | External user identifier when present. |
| `id` | string | Productboard user identifier. |
| `name` | string | User display name. |

## Native endpoint

Through the native Productboard API, this operation is `GET /users` (base URL `https://api.productboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-users.md) for the provider-specific parameters and requirements.

