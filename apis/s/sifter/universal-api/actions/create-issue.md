# Sifter: Create Issue

Creates a new issue in Sifter.

```
POST https://connect.mindcloud.co/v1/universal/sifter/latest/actions/create-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sifter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sifter/latest/actions/create-issue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "subject": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sifter/latest/actions/create-issue', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "subject": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assigneeName` | string | no | The assignee username or name from the project people list. |
| `body` | string | no | The issue description. |
| `categoryName` | string | no | The category name from the project categories list. |
| `milestoneName` | string | no | The milestone name from the project milestones list. |
| `priorityName` | string | no | The priority name from Sifter, for example Normal. |
| `projectId` | number | yes | The Sifter project ID. |
| `subject` | string | yes | The issue title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiUrl": "https://example.com",
      "assigneeEmail": "ava@example.com",
      "assigneeName": "Ava Chen",
      "attachmentCount": 1,
      "categoryName": "Ava Chen",
      "commentCount": 1,
      "comments": [
        {}
      ],
      "createdAt": "string",
      "description": "string",
      "milestoneName": "Ava Chen",
      "number": 1,
      "openerEmail": "ava@example.com",
      "openerName": "Ava Chen",
      "priority": "string",
      "status": "string",
      "subject": "string",
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiUrl` | string |  |
| `assigneeEmail` | string |  |
| `assigneeName` | string |  |
| `attachmentCount` | number |  |
| `categoryName` | string |  |
| `commentCount` | number |  |
| `comments` | array<object> |  |
| `createdAt` | string |  |
| `description` | string |  |
| `milestoneName` | string |  |
| `number` | number |  |
| `openerEmail` | string |  |
| `openerName` | string |  |
| `priority` | string |  |
| `status` | string |  |
| `subject` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Sifter API, this operation is `POST /projects/:project_id/issues` (base URL `https://{{credentials.subdomain}}.sifterapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-issue.md) for the provider-specific parameters and requirements.

