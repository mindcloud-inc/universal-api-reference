# Finmei: List Expenses



```
GET https://connect.mindcloud.co/v1/universal/finmei/latest/actions/list-expenses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finmei `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finmei/latest/actions/list-expenses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finmei/latest/actions/list-expenses?${params}`, {
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
      "data": [
        {
          "createdAt": 1,
          "currency": "string",
          "date": "string",
          "id": "string",
          "seller": "string",
          "total": 1,
          "updatedAt": 1
        }
      ],
      "meta": {
        "currentPage": 1,
        "lastPage": 1,
        "path": "string",
        "perPage": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].createdAt` | number |  |
| `data[].currency` | string |  |
| `data[].date` | string |  |
| `data[].id` | string |  |
| `data[].seller` | string |  |
| `data[].total` | number |  |
| `data[].updatedAt` | number |  |
| `meta.currentPage` | number |  |
| `meta.lastPage` | number |  |
| `meta.path` | string |  |
| `meta.perPage` | number |  |
| `meta.total` | number |  |

## Native endpoint

Through the native Finmei API, this operation is `GET /expenses` (base URL `https://app.finmei.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-expenses.md) for the provider-specific parameters and requirements.

