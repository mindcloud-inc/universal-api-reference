# Sifter: Create Comment

Creates a new comment on a Sifter issue.

```
POST https://connect.mindcloud.co/v1/universal/sifter/latest/actions/create-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sifter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sifter/latest/actions/create-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": "string",
  "issueId": 1,
  "projectId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sifter/latest/actions/create-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": "string",
    "issueId": 1,
    "projectId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | yes | The comment body. |
| `internal` | boolean | no | Set true to make the comment visible only to the primary organization. |
| `issueId` | number | yes | The Sifter issue ID. |
| `projectId` | number | yes | The Sifter project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigneeEmail": "ava@example.com",
      "assigneeName": "Ava Chen",
      "attachments": [
        {}
      ],
      "body": "string",
      "category": "string",
      "commenter": "string",
      "commenterEmail": "ava@example.com",
      "createdAt": "string",
      "internal": true,
      "milestoneName": "Ava Chen",
      "opener": "string",
      "openerEmail": "ava@example.com",
      "priority": "string",
      "project": "string",
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigneeEmail` | string |  |
| `assigneeName` | string |  |
| `attachments` | array<object> |  |
| `body` | string |  |
| `category` | string |  |
| `commenter` | string |  |
| `commenterEmail` | string |  |
| `createdAt` | string |  |
| `internal` | boolean |  |
| `milestoneName` | string |  |
| `opener` | string |  |
| `openerEmail` | string |  |
| `priority` | string |  |
| `project` | string |  |
| `status` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Sifter API, this operation is `POST /projects/:project_id/issues/:issue_id` (base URL `https://{{credentials.subdomain}}.sifterapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-comment.md) for the provider-specific parameters and requirements.

