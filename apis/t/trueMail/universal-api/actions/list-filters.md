# TrueMail: List Filters

Retrieves saved blocklist filters from TrueMail.

```
GET https://connect.mindcloud.co/v1/universal/trueMail/latest/actions/list-filters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrueMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trueMail/latest/actions/list-filters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trueMail/latest/actions/list-filters?${params}`, {
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
| `filterType` | string | no | Optional filter category to return. One of: `0`, `1`, `2`. |
| `page` | number | no | The result page to fetch. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filters": [
        {
          "createdAt": "string",
          "filterType": "string",
          "id": 1,
          "reason": "string",
          "updatedAt": "string",
          "userId": 1,
          "value": "string"
        }
      ],
      "pagination": {
        "currentPage": 1,
        "totalCount": 1,
        "totalPages": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filters` | array<object> |  |
| `filters[].createdAt` | string |  |
| `filters[].filterType` | string |  |
| `filters[].id` | number |  |
| `filters[].reason` | string |  |
| `filters[].updatedAt` | string |  |
| `filters[].userId` | number |  |
| `filters[].value` | string |  |
| `pagination.currentPage` | number |  |
| `pagination.totalCount` | number |  |
| `pagination.totalPages` | number |  |

## Native endpoint

Through the native TrueMail API, this operation is `GET /v1/filters` (base URL `https://api.mailcop.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-filters.md) for the provider-specific parameters and requirements.

