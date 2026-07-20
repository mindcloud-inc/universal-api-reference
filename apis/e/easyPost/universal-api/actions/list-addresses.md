# EasyPost: List Addresses

Retrieves a list of addresses from EasyPost.

```
GET https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/list-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/list-addresses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/list-addresses?${params}`, {
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
      "city": "string",
      "company": "string",
      "country": "string",
      "email": "ava@example.com",
      "id": "string",
      "mode": "string",
      "name": "Ava Chen",
      "object": "string",
      "phone": "string",
      "state": "string",
      "street1": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string | City. |
| `company` | string | Company name. |
| `country` | string | Country. |
| `email` | string | Email address. |
| `id` | string | EasyPost Address ID. |
| `mode` | string | EasyPost mode. |
| `name` | string | Recipient or sender name. |
| `object` | string | EasyPost object type. |
| `phone` | string | Phone number. |
| `state` | string | State. |
| `street1` | string | Street address. |
| `zip` | string | Postal code. |

## Native endpoint

Through the native EasyPost API, this operation is `GET /addresses` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-addresses.md) for the provider-specific parameters and requirements.

