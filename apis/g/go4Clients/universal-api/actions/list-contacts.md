# Go4Clients: List Contacts

Retrieves contacts from Go4Clients.

```
GET https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Go4Clients `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/list-contacts?${params}`, {
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
          "_id": "string",
          "createdOn": "2026-05-07T12:00:00.000Z",
          "height": "string",
          "lastUpdate": "2026-05-07T12:00:00.000Z",
          "Mobile Number": "string",
          "mobileNumber": "string",
          "name": "Ava Chen",
          "sex": "string",
          "source": "string",
          "weight": "string",
          "whiteLabelId": "string"
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
| `content[]._id` | string |  |
| `content[].createdOn` | date |  |
| `content[].height` | string |  |
| `content[].lastUpdate` | date |  |
| `content[].Mobile Number` | string |  |
| `content[].mobileNumber` | string |  |
| `content[].name` | string |  |
| `content[].sex` | string |  |
| `content[].source` | string |  |
| `content[].weight` | string |  |
| `content[].whiteLabelId` | string |  |
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

Through the native Go4Clients API, this operation is `GET /api/groupscontacts/contacts/v1.0/` (base URL `https://cloud.go4clients.com:8580`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

