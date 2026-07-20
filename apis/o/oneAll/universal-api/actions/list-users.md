# OneAll: List Users

Retrieves all site users from OneAll.

```
GET https://connect.mindcloud.co/v1/universal/oneAll/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneAll `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneAll/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneAll/latest/actions/list-users?${params}`, {
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
      "response": {
        "request": {
          "date": "2026-05-07T12:00:00.000Z",
          "resource": "string",
          "status": {
            "code": 1,
            "flag": "string",
            "info": "string"
          }
        },
        "result": {
          "data": {
            "users": {
              "count": 1,
              "pagination": {
                "currentPage": 1,
                "entriesPerPage": 1,
                "order": {
                  "direction": "string",
                  "field": "string"
                },
                "totalEntries": 1,
                "totalPages": 1
              }
            }
          }
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response.request.date` | date |  |
| `response.request.resource` | string |  |
| `response.request.status.code` | number |  |
| `response.request.status.flag` | string |  |
| `response.request.status.info` | string |  |
| `response.result.data.users.count` | number |  |
| `response.result.data.users.pagination.currentPage` | number |  |
| `response.result.data.users.pagination.entriesPerPage` | number |  |
| `response.result.data.users.pagination.order.direction` | string |  |
| `response.result.data.users.pagination.order.field` | string |  |
| `response.result.data.users.pagination.totalEntries` | number |  |
| `response.result.data.users.pagination.totalPages` | number |  |

## Native endpoint

Through the native OneAll API, this operation is `GET /users.json` (base URL `https://mindcloudco.api.oneall.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

