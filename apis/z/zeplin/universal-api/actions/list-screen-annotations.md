# Zeplin: List Screen Annotations

Retrieves a list of screen annotations from Zeplin.

```
GET https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-screen-annotations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-screen-annotations?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=string&screenId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "string",
  "screenId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-screen-annotations?${params}`, {
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
| `screenId` | string | yes | Screen id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "created": 1,
      "creator": {},
      "id": "string",
      "position": {},
      "type": {},
      "updated": 1,
      "updated_by": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `created` | number |  |
| `creator` | object |  |
| `id` | string |  |
| `position` | object |  |
| `type` | object |  |
| `updated` | number |  |
| `updated_by` | object |  |

## Native endpoint

Through the native Zeplin API, this operation is `GET /projects/{project_id}/screens/{screen_id}/annotations` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-screen-annotations.md) for the provider-specific parameters and requirements.

