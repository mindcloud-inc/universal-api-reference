# Hy.page: List People



```
GET https://connect.mindcloud.co/v1/universal/hypage/latest/actions/list-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hy.page `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hypage/latest/actions/list-people?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hypage/latest/actions/list-people?${params}`, {
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
      "category": "string",
      "city": "string",
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "isCustomer": true,
      "metadata": {},
      "name": "Ava Chen",
      "phone": "string",
      "purchaseValue": 1,
      "signupSource": "string",
      "state": "string",
      "tags": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `city` | string |  |
| `country` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `id` | string |  |
| `isCustomer` | boolean |  |
| `metadata` | object |  |
| `name` | string |  |
| `phone` | string |  |
| `purchaseValue` | number |  |
| `signupSource` | string |  |
| `state` | string |  |
| `tags` | array<string> |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Hy.page API, this operation is `GET /hyax-api/v1/people` (base URL `https://platform.hyax.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-people.md) for the provider-specific parameters and requirements.

