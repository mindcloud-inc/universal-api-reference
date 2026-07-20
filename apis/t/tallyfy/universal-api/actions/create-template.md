# Tallyfy: Create Template

Creates a new template in Tallyfy.

```
POST https://connect.mindcloud.co/v1/universal/tallyfy/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tallyfy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tallyfy/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tallyfy/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "allow_launcher_change_name": true,
      "archived_at": "2026-05-07T12:00:00.000Z",
      "auto_naming": true,
      "can_add_oot": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_by": 1,
      "default_process_name_format": "Ava Chen",
      "dual_version_enabled": true,
      "explanation_video": "string",
      "folder_changeable_by_launcher": true,
      "folderize_process": true,
      "id": "string",
      "increment_id": 1,
      "is_featured": true,
      "is_pinned": true,
      "is_public": true,
      "is_public_kickoff": true,
      "is_published_state": true,
      "kickoff_description": "string",
      "kickoff_title": "string",
      "ko_form_blueprint_id": "string",
      "last_updated": "2026-05-07T12:00:00.000Z",
      "last_updated_by": 1,
      "owner_id": 1,
      "replace_state_conditionally": true,
      "started_processes": 1,
      "status": "string",
      "steps_count": 1,
      "summary": "string",
      "tag_process": true,
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `allow_launcher_change_name` | boolean |  |
| `archived_at` | date |  |
| `auto_naming` | boolean |  |
| `can_add_oot` | boolean |  |
| `created_at` | date |  |
| `created_by` | number |  |
| `default_process_name_format` | string |  |
| `dual_version_enabled` | boolean |  |
| `explanation_video` | string |  |
| `folder_changeable_by_launcher` | boolean |  |
| `folderize_process` | boolean |  |
| `id` | string |  |
| `increment_id` | number |  |
| `is_featured` | boolean |  |
| `is_pinned` | boolean |  |
| `is_public` | boolean |  |
| `is_public_kickoff` | boolean |  |
| `is_published_state` | boolean |  |
| `kickoff_description` | string |  |
| `kickoff_title` | string |  |
| `ko_form_blueprint_id` | string |  |
| `last_updated` | date |  |
| `last_updated_by` | number |  |
| `owner_id` | number |  |
| `replace_state_conditionally` | boolean |  |
| `started_processes` | number |  |
| `status` | string |  |
| `steps_count` | number |  |
| `summary` | string |  |
| `tag_process` | boolean |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Tallyfy API, this operation is `POST /organizations/:org/checklists` (base URL `https://api.tallyfy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

