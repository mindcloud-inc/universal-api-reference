# Pabbly Hook: Filter Requests



```
GET https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/filter-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Hook `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/filter-requests?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/filter-requests?${params}`, {
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
| `connectionId` | string | no | Connection ID selector. Example: `conn_38657a4a43544e4fa9a911696d72a20e`. |
| `requestId` | string | no | Request ID selector. Example: `req_e038786447e14a2e9282f69229d809a1`. |
| `status` | string | no | Request status selector. Example: `blocked`. |
| `dateRange` | string | no | Date range selector, for example YYYY-MM-DD,YYYY-MM-DD. Example: `2024-05-01,2024-06-31`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentPage": 1,
      "data": [
        {}
      ],
      "page": 1,
      "total": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPage` | number | Current page number. |
| `data` | array<object> | Request records returned by Pabbly Hook. |
| `page` | number | Current page number when returned as page. |
| `total` | number | Total matching request records. |
| `totalPages` | number | Total number of pages. |

## Native endpoint

Through the native Pabbly Hook API, this operation is `GET /api/v1/requests` (base URL `https://hook.pabbly.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/filter-requests.md) for the provider-specific parameters and requirements.

