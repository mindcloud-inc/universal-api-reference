# Clio Manage: List Allocations

Retrieves allocations from your Clio Manage account.

```
GET https://connect.mindcloud.co/v1/universal/clio/latest/actions/list-allocations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clio Manage `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clio/latest/actions/list-allocations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clio/latest/actions/list-allocations?${params}`, {
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
      "amount": 1,
      "date": "string",
      "etag": "string",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | The total amount of money allocated. |
| `date` | string | The date the allocation was applied. |
| `etag` | string | ETag for the Allocation. |
| `id` | number | Unique identifier for the Allocation. |

## Native endpoint

Through the native Clio Manage API, this operation is `GET /allocations.json` (base URL `https://app.clio.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-allocations.md) for the provider-specific parameters and requirements.

