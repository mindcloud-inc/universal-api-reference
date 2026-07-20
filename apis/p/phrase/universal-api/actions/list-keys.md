# Phrase: List Keys

Retrieves translation keys for a project from Phrase.

```
GET https://connect.mindcloud.co/v1/universal/phrase/latest/actions/list-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Phrase `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phrase/latest/actions/list-keys?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phrase/latest/actions/list-keys?${params}`, {
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
| `branch` | string | no | Optional project branch name to scope key results. |
| `localeId` | string | no | Optional locale id used for translated or untranslated key filters. |
| `order` | string | no | Optional sort direction such as asc or desc. |
| `projectId` | string | yes | Phrase project id whose keys should be listed. |
| `q` | string | no | Optional Phrase search query for key names and supported qualifiers. |
| `sort` | string | no | Optional Phrase key sort field such as name, created_at, or updated_at. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "data_type": "string",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "name_hash": "Ava Chen",
      "plural": true,
      "tags": [
        "string"
      ],
      "updated_at": "2026-05-07T12:00:00.000Z",
      "use_ordinal_rules": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `data_type` | string |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `name_hash` | string |  |
| `plural` | boolean |  |
| `tags` | array<string> |  |
| `updated_at` | date |  |
| `use_ordinal_rules` | boolean |  |

## Native endpoint

Through the native Phrase API, this operation is `GET /projects/{project_id}/keys` (base URL `https://api.phrase.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-keys.md) for the provider-specific parameters and requirements.

