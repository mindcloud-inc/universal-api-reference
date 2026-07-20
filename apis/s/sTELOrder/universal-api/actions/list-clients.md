# STEL Order: List Clients

Retrieves a list of clients from STEL Order.

```
GET https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a STEL Order `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-clients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-clients?${params}`, {
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
      "comments": {},
      "deleted": true,
      "email": "ava@example.com",
      "fax": {},
      "id": 1,
      "name": "Ava Chen",
      "path": "string",
      "phone": "string",
      "phone2": {},
      "reference": "string",
      "website": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | object |  |
| `deleted` | boolean |  |
| `email` | string |  |
| `fax` | object |  |
| `id` | number |  |
| `name` | string |  |
| `path` | string |  |
| `phone` | string |  |
| `phone2` | object |  |
| `reference` | string |  |
| `website` | object |  |

## Native endpoint

Through the native STEL Order API, this operation is `GET /clients` (base URL `https://app.stelorder.com/app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

