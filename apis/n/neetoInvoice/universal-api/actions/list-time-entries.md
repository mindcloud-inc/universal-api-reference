# NeetoInvoice: List Time Entries

Retrieves unbilled time entries from NeetoInvoice.

```
GET https://connect.mindcloud.co/v1/universal/neetoInvoice/latest/actions/list-time-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeetoInvoice `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neetoInvoice/latest/actions/list-time-entries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neetoInvoice/latest/actions/list-time-entries?${params}`, {
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
| `projectId` | string | no | Optional project filter for time entries. |
| `userId` | string | no | Optional user filter for time entries. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "currentPageNumber": 1,
        "pageSize": 1,
        "totalPages": 1,
        "totalRecords": 1
      },
      "timeEntries": [
        {
          "duration": 1,
          "id": "string",
          "note": "string",
          "projectId": "string",
          "userId": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination.currentPageNumber` | number |  |
| `pagination.pageSize` | number |  |
| `pagination.totalPages` | number |  |
| `pagination.totalRecords` | number |  |
| `timeEntries[].duration` | number |  |
| `timeEntries[].id` | string |  |
| `timeEntries[].note` | string |  |
| `timeEntries[].projectId` | string |  |
| `timeEntries[].userId` | string |  |

## Native endpoint

Through the native NeetoInvoice API, this operation is `GET /time_entries` (base URL `https://{{credentials.workspaceSubdomain}}.neetoinvoice.com/api/external/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-time-entries.md) for the provider-specific parameters and requirements.

