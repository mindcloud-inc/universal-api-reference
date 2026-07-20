# Skyvern: List Folders

Retrieves workflow folders for your organization from Skyvern.

```
GET https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/list-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skyvern `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/list-folders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/list-folders?${params}`, {
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
| `search` | string | no | Search folders by title or description |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "folder_id": "string",
      "modified_at": "2026-05-07T12:00:00.000Z",
      "organization_id": "string",
      "title": "string",
      "workflow_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Folder creation timestamp |
| `description` | string | Folder description |
| `folder_id` | string | Folder ID |
| `modified_at` | date | Folder modification timestamp |
| `organization_id` | string | Organization ID |
| `title` | string | Folder title |
| `workflow_count` | number | Number of workflows in the folder |

## Native endpoint

Through the native Skyvern API, this operation is `GET /v1/folders` (base URL `https://api.skyvern.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-folders.md) for the provider-specific parameters and requirements.

