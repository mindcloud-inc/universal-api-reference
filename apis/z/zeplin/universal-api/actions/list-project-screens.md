# Zeplin: List Project Screens

Retrieves a list of project screens from Zeplin.

```
GET https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-project-screens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-project-screens?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-project-screens?${params}`, {
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
| `projectId` | string | yes | Project id |
| `sectionId` | string | no | Filter by section id |
| `sort` | string | no | Sort screens by their `section` or their `created` date |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "description": "string",
      "id": "string",
      "image": {},
      "name": "Ava Chen",
      "number_of_annotations": 1,
      "number_of_notes": 1,
      "number_of_versions": 1,
      "section": {},
      "tags": [
        "string"
      ],
      "updated": 1,
      "variant": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number |  |
| `description` | string |  |
| `id` | string |  |
| `image` | object |  |
| `name` | string |  |
| `number_of_annotations` | number |  |
| `number_of_notes` | number |  |
| `number_of_versions` | number |  |
| `section` | object |  |
| `tags` | array<string> |  |
| `updated` | number |  |
| `variant` | object |  |

## Native endpoint

Through the native Zeplin API, this operation is `GET /projects/{project_id}/screens` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-screens.md) for the provider-specific parameters and requirements.

