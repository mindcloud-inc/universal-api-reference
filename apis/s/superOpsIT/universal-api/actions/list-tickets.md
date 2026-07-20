# SuperOps IT: List Tickets



```
GET https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/list-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperOps IT `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/list-tickets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/list-tickets?${params}`, {
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
      "getTicketList": {
        "listInfo": {
          "page": 1,
          "pageSize": 1,
          "totalCount": 1
        },
        "tickets": [
          {
            "createdTime": "2026-05-07T12:00:00.000Z",
            "displayId": "string",
            "requester": {
              "name": "Ava Chen",
              "userId": "string"
            },
            "site": {
              "id": "string",
              "name": "Ava Chen"
            },
            "status": "string",
            "subject": "string",
            "ticketId": "string",
            "updatedTime": "2026-05-07T12:00:00.000Z"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `getTicketList.listInfo.page` | number |  |
| `getTicketList.listInfo.pageSize` | number |  |
| `getTicketList.listInfo.totalCount` | number |  |
| `getTicketList.tickets[].createdTime` | date |  |
| `getTicketList.tickets[].displayId` | string |  |
| `getTicketList.tickets[].requester.name` | string |  |
| `getTicketList.tickets[].requester.userId` | string |  |
| `getTicketList.tickets[].site.id` | string |  |
| `getTicketList.tickets[].site.name` | string |  |
| `getTicketList.tickets[].status` | string |  |
| `getTicketList.tickets[].subject` | string |  |
| `getTicketList.tickets[].ticketId` | string |  |
| `getTicketList.tickets[].updatedTime` | date |  |

## Native endpoint

Through the native SuperOps IT API, this operation is `POST /it` (base URL `https://api.superops.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tickets.md) for the provider-specific parameters and requirements.

