# Leiga: Search Issues

Finds issues in Leiga using paginated project filters.

```
GET https://connect.mindcloud.co/v1/universal/leiga/latest/actions/search-issues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leiga `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leiga/latest/actions/search-issues?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leiga/latest/actions/search-issues?${params}`, {
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
| `projectId` | number | yes | Project ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigneeId": 1,
      "assigneeName": "Ava Chen",
      "createTime": 1,
      "customFieldData": {},
      "dueDate": 1,
      "id": 1,
      "issueTypeId": 1,
      "issueTypeName": "Ava Chen",
      "priorityId": 1,
      "priorityName": "Ava Chen",
      "sprintId": 1,
      "sprintName": "Ava Chen",
      "startDate": 1,
      "statusId": 1,
      "statusName": "Ava Chen",
      "summary": "string",
      "tags": [
        {}
      ],
      "updateTime": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigneeId` | number | Assignee ID. |
| `assigneeName` | string | Assignee name. |
| `createTime` | number | Creation timestamp. |
| `customFieldData` | object | Custom field payload. |
| `dueDate` | number | Due timestamp. |
| `id` | number | Issue ID. |
| `issueTypeId` | number | Issue type ID. |
| `issueTypeName` | string | Issue type name. |
| `priorityId` | number | Priority ID. |
| `priorityName` | string | Priority name. |
| `sprintId` | number | Sprint ID. |
| `sprintName` | string | Sprint name. |
| `startDate` | number | Start timestamp. |
| `statusId` | number | Status ID. |
| `statusName` | string | Status name. |
| `summary` | string | Issue summary. |
| `tags` | array<object> | Tag entries. |
| `updateTime` | number | Last update timestamp. |

## Native endpoint

Through the native Leiga API, this operation is `POST /issue/page` (base URL `https://app.leiga.com/openapi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-issues.md) for the provider-specific parameters and requirements.

