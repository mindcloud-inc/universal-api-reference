# Quire: List Projects

Retrieves projects from Quire.

```
GET https://connect.mindcloud.co/v1/universal/quire/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quire/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quire/latest/actions/list-projects?${params}`, {
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
      "activeCount": 1,
      "attachments": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "description": "string",
      "descriptionHtml": "string",
      "descriptionText": "string",
      "editedAt": "2026-05-07T12:00:00.000Z",
      "followers": [
        {}
      ],
      "iconColor": "string",
      "id": "string",
      "image": "string",
      "name": "Ava Chen",
      "nameHtml": "Ava Chen",
      "nameText": "Ava Chen",
      "oid": "string",
      "organization": {},
      "rootCount": 1,
      "taskCount": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeCount` | number |  |
| `attachments` | array<object> |  |
| `createdAt` | date |  |
| `createdBy` | object |  |
| `description` | string |  |
| `descriptionHtml` | string |  |
| `descriptionText` | string |  |
| `editedAt` | date |  |
| `followers` | array<object> |  |
| `iconColor` | string |  |
| `id` | string |  |
| `image` | string |  |
| `name` | string |  |
| `nameHtml` | string |  |
| `nameText` | string |  |
| `oid` | string |  |
| `organization` | object |  |
| `rootCount` | number |  |
| `taskCount` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Quire API, this operation is `GET project/list` (base URL `https://quire.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

