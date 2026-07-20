# Phrase: List Locales

Retrieves locales for a project from Phrase.

```
GET https://connect.mindcloud.co/v1/universal/phrase/latest/actions/list-locales
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Phrase `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phrase/latest/actions/list-locales?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phrase/latest/actions/list-locales?${params}`, {
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
| `branch` | string | no | Optional project branch name to scope locale results. |
| `projectId` | string | yes | Phrase project id whose locales should be listed. |
| `sortBy` | string | no | Optional Phrase locale sort order such as name_asc or default_desc. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "default": true,
      "fallback_locale": {},
      "id": "string",
      "main": true,
      "name": "Ava Chen",
      "ordinal_plural_forms": [
        "string"
      ],
      "plural_forms": [
        "string"
      ],
      "rtl": true,
      "source_locale": {},
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `created_at` | date |  |
| `default` | boolean |  |
| `fallback_locale` | object |  |
| `id` | string |  |
| `main` | boolean |  |
| `name` | string |  |
| `ordinal_plural_forms` | array<string> |  |
| `plural_forms` | array<string> |  |
| `rtl` | boolean |  |
| `source_locale` | object |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Phrase API, this operation is `GET /projects/{project_id}/locales` (base URL `https://api.phrase.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-locales.md) for the provider-specific parameters and requirements.

