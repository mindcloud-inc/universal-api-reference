# Productlane: Get Changelog

Retrieves a changelog from your Productlane workspace.

```
GET https://connect.mindcloud.co/v1/universal/productlane/latest/actions/get-changelog
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productlane/latest/actions/get-changelog?connectionId=$CONNECTION_ID&workspaceId=string&changelogId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "changelogId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productlane/latest/actions/get-changelog?${params}`, {
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
| `workspaceId` | string | yes |  |
| `changelogId` | string | yes |  |
| `language` | string | no |  |

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

Through the native Productlane API, this operation is `GET /changelogs/:workspaceId/:changelogId` (base URL `https://productlane.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-changelog.md) for the provider-specific parameters and requirements.

