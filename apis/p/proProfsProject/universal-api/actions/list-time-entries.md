# ProProfs Project: List Time Entries

Retrieves a list of time entries from ProProfs Project.

```
GET https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-time-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProProfs Project `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-time-entries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-time-entries?${params}`, {
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
| `clientId` | string | no | Filter time entries by client. |
| `limit` | string | no | Limit the number of returned time entries. |
| `offset` | string | no | Offset for returned time entries. |
| `projectId` | string | no | Filter time entries by project ID. |
| `subtaskId` | string | no | Filter time entries by subtask ID. |
| `taskId` | string | no | Filter time entries by task ID. |
| `userId` | string | no | Filter time entries by user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "billed": 1,
          "date": "string",
          "dateStarted": "string",
          "dateStopped": "string",
          "description": "string",
          "entryId": "string",
          "hours": 1,
          "minutes": 1,
          "projectId": "string",
          "projectName": "Ava Chen",
          "seconds": "string",
          "subtaskId": "string",
          "subtaskName": "Ava Chen",
          "taskId": "string",
          "taskName": "Ava Chen",
          "userId": "string",
          "userName": "Ava Chen"
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
| `data[].billed` | number |  |
| `data[].date` | string |  |
| `data[].dateStarted` | string |  |
| `data[].dateStopped` | string |  |
| `data[].description` | string |  |
| `data[].entryId` | string |  |
| `data[].hours` | number |  |
| `data[].minutes` | number |  |
| `data[].projectId` | string |  |
| `data[].projectName` | string |  |
| `data[].seconds` | string |  |
| `data[].subtaskId` | string |  |
| `data[].subtaskName` | string |  |
| `data[].taskId` | string |  |
| `data[].taskName` | string |  |
| `data[].userId` | string |  |
| `data[].userName` | string |  |
| `paging.limit` | number |  |
| `paging.offset` | number |  |
| `paging.totalRecords` | number |  |

## Native endpoint

Through the native ProProfs Project API, this operation is `GET /time_entries` (base URL `https://api.projectbubble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-time-entries.md) for the provider-specific parameters and requirements.

