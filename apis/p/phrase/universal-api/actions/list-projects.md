# Phrase: List Projects

Retrieves a list of projects from Phrase.

```
GET https://connect.mindcloud.co/v1/universal/phrase/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Phrase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phrase/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phrase/latest/actions/list-projects?${params}`, {
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
| `accountId` | string | no | Optional Phrase account id to scope returned projects. |
| `sortBy` | string | no | Optional Phrase project sort order such as name_asc or updated_at_desc. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {},
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "main_format": "string",
      "name": "Ava Chen",
      "point_of_contact": {},
      "project_image_url": "https://example.com",
      "slug": "string",
      "space": {},
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | object |  |
| `created_at` | date |  |
| `id` | string |  |
| `main_format` | string |  |
| `name` | string |  |
| `point_of_contact` | object |  |
| `project_image_url` | string |  |
| `slug` | string |  |
| `space` | object |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Phrase API, this operation is `GET /projects` (base URL `https://api.phrase.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

