# Supabugs: Delete Issue Comment

Deletes a comment from a Supabugs issue.

```
DELETE https://connect.mindcloud.co/v1/universal/supabugs/latest/actions/delete-issue-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supabugs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/supabugs/latest/actions/delete-issue-comment?connectionId=$CONNECTION_ID&issueId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "issueId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supabugs/latest/actions/delete-issue-comment?${params}`, {
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
| `issueId` | string | yes | Supabugs issue id. |
| `id` | string | yes | Supabugs comment id. |

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

Through the native Supabugs API, this operation is `DELETE /issues/:issueId/comments/:id` (base URL `https://api.supabugs.io/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-issue-comment.md) for the provider-specific parameters and requirements.

