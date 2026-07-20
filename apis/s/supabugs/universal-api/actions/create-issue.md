# Supabugs: Create Issue

Creates a new issue in Supabugs.

```
POST https://connect.mindcloud.co/v1/universal/supabugs/latest/actions/create-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supabugs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/supabugs/latest/actions/create-issue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "description": "string",
  "type": "string",
  "severity": "string",
  "priority": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/supabugs/latest/actions/create-issue', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "description": "string",
    "type": "string",
    "severity": "string",
    "priority": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Issue title. |
| `description` | string | yes | Issue description. |
| `type` | string | yes | Bug type id from List Bug Types. |
| `severity` | string | yes | Bug severity id from List Bug Severities. |
| `priority` | string | yes | Bug priority id from List Bug Priorities. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "assignees": [
        {}
      ],
      "attachments": [
        {}
      ],
      "closed": true,
      "closedAt": "2026-05-07T12:00:00.000Z",
      "code": "string",
      "comments": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdById": "string",
      "createdByUser": {},
      "description": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "environment": {},
      "history": [
        {}
      ],
      "id": "string",
      "issuedId": "string",
      "issuedType": "string",
      "priority": {},
      "priorityId": "string",
      "project": {},
      "projectId": "string",
      "publicShareLink": "https://example.com",
      "relatedToIssue": "string",
      "relatedToIssueId": "string",
      "severity": {},
      "severityId": "string",
      "status": {},
      "statusId": "string",
      "title": "string",
      "type": {},
      "typeId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedById": "string",
      "updatedByUser": {},
      "watchers": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `assignees` | array<object> |  |
| `attachments` | array<object> |  |
| `closed` | boolean |  |
| `closedAt` | date |  |
| `code` | string |  |
| `comments` | array<object> |  |
| `createdAt` | date |  |
| `createdById` | string |  |
| `createdByUser` | object |  |
| `description` | string |  |
| `dueDate` | date |  |
| `environment` | object |  |
| `history` | array<object> |  |
| `id` | string |  |
| `issuedId` | string |  |
| `issuedType` | string |  |
| `priority` | object |  |
| `priorityId` | string |  |
| `project` | object |  |
| `projectId` | string |  |
| `publicShareLink` | string |  |
| `relatedToIssue` | string |  |
| `relatedToIssueId` | string |  |
| `severity` | object |  |
| `severityId` | string |  |
| `status` | object |  |
| `statusId` | string |  |
| `title` | string |  |
| `type` | object |  |
| `typeId` | string |  |
| `updatedAt` | date |  |
| `updatedById` | string |  |
| `updatedByUser` | object |  |
| `watchers` | array<object> |  |

## Native endpoint

Through the native Supabugs API, this operation is `POST /issues` (base URL `https://api.supabugs.io/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-issue.md) for the provider-specific parameters and requirements.

