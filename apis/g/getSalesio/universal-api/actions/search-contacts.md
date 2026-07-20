# GetSales.io: List Contacts



```
GET https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/search-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetSales.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/search-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/search-contacts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | object | no | Filters to apply when searching contacts. Example: `[object Object]`. |
| `limit` | number | no | Number of contacts to return. Default: `20`. Example: `20`. |
| `offset` | number | no | Number of contacts to skip. Default: `0`. Example: `0`. |
| `orderField` | string | no | Field to sort by. Default: `created_at`. Example: `created_at`. |
| `orderType` | list | no | Sorting direction. One of: `0`, `1`. Default: `desc`. |
| `disableAggregation` | boolean | no | When true, disables contact data aggregation. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "limit": 1,
      "offset": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `limit` | number |  |
| `offset` | number |  |
| `total` | number |  |

## Native endpoint

Through the native GetSales.io API, this operation is `POST /leads/api/leads/search` (base URL `https://amazing.getsales.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-contacts.md) for the provider-specific parameters and requirements.

