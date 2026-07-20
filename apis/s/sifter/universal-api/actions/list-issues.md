# Sifter: List Issues

Retrieves issues for a project from Sifter.

```
GET https://connect.mindcloud.co/v1/universal/sifter/latest/actions/list-issues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sifter `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sifter/latest/actions/list-issues?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sifter/latest/actions/list-issues?${params}`, {
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
| `assigneeIds` | string | no |  |
| `categoryIds` | string | no |  |
| `milestoneIds` | string | no |  |
| `priorityIds` | string | no | One or more priority IDs separated by hyphens, for example 1-2. |
| `projectId` | number | yes | The Sifter project ID. |
| `searchQuery` | string | no | Search issue text. |
| `statusIds` | string | no | One or more status IDs separated by hyphens, for example 209607-209608. |

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

Through the native Sifter API, this operation is `GET /projects/:project_id/issues` (base URL `https://{{credentials.subdomain}}.sifterapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-issues.md) for the provider-specific parameters and requirements.

