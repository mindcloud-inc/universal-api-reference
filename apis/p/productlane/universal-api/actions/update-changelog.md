# Productlane: Update Changelog

Updates an existing changelog in Productlane.

```
PUT https://connect.mindcloud.co/v1/universal/productlane/latest/actions/update-changelog
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/productlane/latest/actions/update-changelog" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/productlane/latest/actions/update-changelog', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `title` | string | no |  |
| `content` | string | no |  |
| `date` | date | no |  |
| `published` | boolean | no |  |
| `archived` | boolean | no |  |
| `tagIds[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "date": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "imageUrl": "https://example.com",
      "isDeleted": true,
      "notes": {},
      "projectId": "string",
      "published": true,
      "tags": [
        {}
      ],
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "version": 1,
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `createdAt` | date |  |
| `date` | date |  |
| `id` | string |  |
| `imageUrl` | string |  |
| `isDeleted` | boolean |  |
| `notes` | object |  |
| `projectId` | string |  |
| `published` | boolean |  |
| `tags` | array<object> |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `version` | number |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Productlane API, this operation is `PATCH /changelogs/:id` (base URL `https://productlane.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-changelog.md) for the provider-specific parameters and requirements.

