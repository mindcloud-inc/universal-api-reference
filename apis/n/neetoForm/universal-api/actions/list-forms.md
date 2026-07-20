# NeetoForm: List Forms

Retrieves forms from a NeetoForm workspace.

```
GET https://connect.mindcloud.co/v1/universal/neetoForm/latest/actions/list-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeetoForm `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neetoForm/latest/actions/list-forms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neetoForm/latest/actions/list-forms?${params}`, {
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
      "forms": [
        {
          "attemptUrl": "https://example.com",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "createdBy": "string",
          "id": "string",
          "isArchived": true,
          "isDisabled": true,
          "isPublished": true,
          "isSuspended": true,
          "state": "string",
          "submissionsCount": 1,
          "title": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "pagination": {
        "currentPageNumber": 1,
        "pageSize": 1,
        "totalPages": 1,
        "totalRecords": 1
      },
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `forms[].attemptUrl` | string |  |
| `forms[].createdAt` | date |  |
| `forms[].createdBy` | string |  |
| `forms[].id` | string |  |
| `forms[].isArchived` | boolean |  |
| `forms[].isDisabled` | boolean |  |
| `forms[].isPublished` | boolean |  |
| `forms[].isSuspended` | boolean |  |
| `forms[].state` | string |  |
| `forms[].submissionsCount` | number |  |
| `forms[].title` | string |  |
| `forms[].updatedAt` | date |  |
| `pagination.currentPageNumber` | number |  |
| `pagination.pageSize` | number |  |
| `pagination.totalPages` | number |  |
| `pagination.totalRecords` | number |  |
| `totalCount` | number |  |

## Native endpoint

Through the native NeetoForm API, this operation is `GET /forms` (base URL `https://{{credentials.workspaceSubdomain}}.neetoform.com/api/external/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-forms.md) for the provider-specific parameters and requirements.

