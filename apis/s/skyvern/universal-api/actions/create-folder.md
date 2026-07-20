# Skyvern: Create Folder

Creates a new workflow folder in Skyvern.

```
POST https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/create-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skyvern `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/create-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Folder description |
| `title` | string | yes | Folder title |

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

Through the native Skyvern API, this operation is `POST /v1/folders` (base URL `https://api.skyvern.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-folder.md) for the provider-specific parameters and requirements.

