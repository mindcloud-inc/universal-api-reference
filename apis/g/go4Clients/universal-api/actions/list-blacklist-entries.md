# Go4Clients: List Blacklist Entries

Retrieves blacklist entries from Go4Clients.

```
GET https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/list-blacklist-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Go4Clients `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/list-blacklist-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/list-blacklist-entries?${params}`, {
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
      "content": [
        {
          "blacklistId": "string",
          "createdOn": "string",
          "number": "string",
          "programId": "string",
          "programName": "Ava Chen",
          "service": "string",
          "status": "string"
        }
      ],
      "first": true,
      "last": true,
      "number": 1,
      "numberOfElements": 1,
      "pageable": {
        "offset": 1,
        "paged": true,
        "pageNumber": 1,
        "pageSize": 1,
        "sort": {
          "sorted": true,
          "unsorted": true
        },
        "unpaged": true
      },
      "size": 1,
      "sort": {
        "sorted": true,
        "unsorted": true
      },
      "totalElements": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content[].blacklistId` | string |  |
| `content[].createdOn` | string |  |
| `content[].number` | string |  |
| `content[].programId` | string |  |
| `content[].programName` | string |  |
| `content[].service` | string |  |
| `content[].status` | string |  |
| `first` | boolean |  |
| `last` | boolean |  |
| `number` | number |  |
| `numberOfElements` | number |  |
| `pageable.offset` | number |  |
| `pageable.paged` | boolean |  |
| `pageable.pageNumber` | number |  |
| `pageable.pageSize` | number |  |
| `pageable.sort.sorted` | boolean |  |
| `pageable.sort.unsorted` | boolean |  |
| `pageable.unpaged` | boolean |  |
| `size` | number |  |
| `sort.sorted` | boolean |  |
| `sort.unsorted` | boolean |  |
| `totalElements` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Go4Clients API, this operation is `GET /api/blacklist/v1.0/` (base URL `https://cloud.go4clients.com:8580`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-blacklist-entries.md) for the provider-specific parameters and requirements.

