# Zeplin: List Screen Sections

Retrieves a list of screen sections from Zeplin.

```
GET https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-screen-sections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-screen-sections?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-screen-sections?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "id": "string",
      "name": "Ava Chen",
      "parent": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number |  |
| `id` | string |  |
| `name` | string |  |
| `parent` | object |  |

## Native endpoint

Through the native Zeplin API, this operation is `GET /projects/{project_id}/screen_sections` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-screen-sections.md) for the provider-specific parameters and requirements.

