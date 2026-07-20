# DitLead: Get Lists



```
GET https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/get-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DitLead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/get-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/get-lists?${params}`, {
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
| `page` | number | no |  |
| `pageSize` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "lists": [
          {}
        ],
        "pagination": {
          "page": 1,
          "pageSize": 1,
          "totalCount": 1,
          "totalPages": 1
        }
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.lists` | array<object> |  |
| `data.pagination.page` | number |  |
| `data.pagination.pageSize` | number |  |
| `data.pagination.totalCount` | number |  |
| `data.pagination.totalPages` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native DitLead API, this operation is `GET /v1/list` (base URL `https://api.ditlead.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lists.md) for the provider-specific parameters and requirements.

