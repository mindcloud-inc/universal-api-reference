# Go4Clients: List Groups

Retrieves contact groups from Go4Clients.

```
GET https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/list-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Go4Clients `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/list-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/list-groups?${params}`, {
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
          "createdOn": "2026-05-07T12:00:00.000Z",
          "filterParameters": [
            {
              "canonicalFilterClass": "string",
              "filterClass": "string",
              "key": "string",
              "type": "string",
              "value": "string"
            }
          ],
          "groupName": "Ava Chen",
          "Id": "string",
          "lastUpdate": "2026-05-07T12:00:00.000Z",
          "organizationId": "string",
          "organizationName": "Ava Chen",
          "showFilterParameters": [
            {
              "canonicalFilterClass": "string",
              "filterClass": "string",
              "key": "string",
              "type": "string",
              "value": "string"
            }
          ],
          "source": "string",
          "userId": "string",
          "userName": "Ava Chen",
          "whitelabelId": "string"
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
| `content[].createdOn` | date |  |
| `content[].filterParameters[].canonicalFilterClass` | string |  |
| `content[].filterParameters[].filterClass` | string |  |
| `content[].filterParameters[].key` | string |  |
| `content[].filterParameters[].type` | string |  |
| `content[].filterParameters[].value` | string |  |
| `content[].groupName` | string |  |
| `content[].Id` | string |  |
| `content[].lastUpdate` | date |  |
| `content[].organizationId` | string |  |
| `content[].organizationName` | string |  |
| `content[].showFilterParameters[].canonicalFilterClass` | string |  |
| `content[].showFilterParameters[].filterClass` | string |  |
| `content[].showFilterParameters[].key` | string |  |
| `content[].showFilterParameters[].type` | string |  |
| `content[].showFilterParameters[].value` | string |  |
| `content[].source` | string |  |
| `content[].userId` | string |  |
| `content[].userName` | string |  |
| `content[].whitelabelId` | string |  |
| `first` | boolean |  |
| `last` | boolean |  |
| `number` | number |  |
| `numberOfElements` | number |  |
| `pageable.offset` | number |  |
| `pageable.paged` | boolean |  |
| `pageable.pageNumber` | number |  |
| `pageable.pageSize` | number |  |
| `pageable.unpaged` | boolean |  |
| `size` | number |  |
| `sort.sorted` | boolean |  |
| `sort.unsorted` | boolean |  |
| `totalElements` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Go4Clients API, this operation is `GET /api/groupscontacts/groups/v1.0/` (base URL `https://cloud.go4clients.com:8580`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-groups.md) for the provider-specific parameters and requirements.

