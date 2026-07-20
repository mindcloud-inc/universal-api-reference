# Sifter: Get Issue

Retrieves a specific issue from Sifter.

```
GET https://connect.mindcloud.co/v1/universal/sifter/latest/actions/get-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sifter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sifter/latest/actions/get-issue?connectionId=$CONNECTION_ID&issueId=1&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "issueId": "1",
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sifter/latest/actions/get-issue?${params}`, {
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
| `issueId` | number | yes | The Sifter issue ID. |
| `projectId` | number | yes | The Sifter project ID. |

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

Through the native Sifter API, this operation is `GET /projects/:project_id/issues/:issue_id` (base URL `https://{{credentials.subdomain}}.sifterapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-issue.md) for the provider-specific parameters and requirements.

