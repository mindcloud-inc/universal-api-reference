# Phrase: List Translations

Retrieves translations for a project from Phrase.

```
GET https://connect.mindcloud.co/v1/universal/phrase/latest/actions/list-translations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Phrase `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phrase/latest/actions/list-translations?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phrase/latest/actions/list-translations?${params}`, {
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
| `branch` | string | no | Optional project branch name to scope translation results. |
| `order` | string | no | Optional sort direction such as asc or desc. |
| `projectId` | string | yes | Phrase project id whose translations should be listed. |
| `q` | string | no | Optional Phrase search query for translation content. |
| `sort` | string | no | Optional Phrase translation sort field such as key_name, created_at, or updated_at. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "excluded": true,
      "id": "string",
      "key": {},
      "linked_translation": {},
      "locale": {},
      "placeholders": [
        "string"
      ],
      "plural_suffix": "string",
      "state": "string",
      "unverified": true,
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `created_at` | date |  |
| `excluded` | boolean |  |
| `id` | string |  |
| `key` | object |  |
| `linked_translation` | object |  |
| `locale` | object |  |
| `placeholders` | array<string> |  |
| `plural_suffix` | string |  |
| `state` | string |  |
| `unverified` | boolean |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Phrase API, this operation is `GET /projects/{project_id}/translations` (base URL `https://api.phrase.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-translations.md) for the provider-specific parameters and requirements.

