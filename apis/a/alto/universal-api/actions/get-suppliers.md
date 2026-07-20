# Alto: Get Suppliers

Retrieves supplier records from your Alto account.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-suppliers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-suppliers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-suppliers?${params}`, {
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
      "branchId": "string",
      "companyName": "Ava Chen",
      "id": "string",
      "notes": "string",
      "providedServices": [
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
| `branchId` | string |  |
| `companyName` | string |  |
| `id` | string |  |
| `notes` | string |  |
| `providedServices` | array<object> |  |

## Native endpoint

Through the native Alto API, this operation is `GET /suppliers` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-suppliers.md) for the provider-specific parameters and requirements.

