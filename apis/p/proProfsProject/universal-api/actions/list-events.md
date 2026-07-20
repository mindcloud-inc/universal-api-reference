# ProProfs Project: List Events

Retrieves a list of events from ProProfs Project.

```
GET https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProProfs Project `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-events?${params}`, {
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
| `dueDateFrom` | string | no | Filter events with a due date on or after this date. |
| `dueDateTo` | string | no | Filter events with a due date on or before this date. |
| `limit` | string | no | Limit the number of returned events. |
| `offset` | string | no | Offset for returned events. |
| `projectId` | string | no | Filter events by project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "dateCreated": "string",
          "dateModified": "string",
          "dueDate": "string",
          "eventId": "string",
          "eventName": "Ava Chen",
          "projectId": "string",
          "startDate": "string",
          "userId": "string"
        }
      ],
      "paging": {
        "limit": 1,
        "offset": 1,
        "totalRecords": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].dateCreated` | string |  |
| `data[].dateModified` | string |  |
| `data[].dueDate` | string |  |
| `data[].eventId` | string |  |
| `data[].eventName` | string |  |
| `data[].projectId` | string |  |
| `data[].startDate` | string |  |
| `data[].userId` | string |  |
| `paging.limit` | number |  |
| `paging.offset` | number |  |
| `paging.totalRecords` | number |  |

## Native endpoint

Through the native ProProfs Project API, this operation is `GET /events` (base URL `https://api.projectbubble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

