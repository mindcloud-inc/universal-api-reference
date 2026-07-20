# Zeplin: List Screen Notes

Retrieves a list of screen notes from Zeplin.

```
GET https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-screen-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-screen-notes?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=string&screenId=string" \
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

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-screen-notes?${params}`, {
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
      "color": {},
      "comments": [
        {}
      ],
      "created": 1,
      "creator": {},
      "id": "string",
      "order": 1,
      "position": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | object |  |
| `comments` | array<object> |  |
| `created` | number |  |
| `creator` | object |  |
| `id` | string |  |
| `order` | number |  |
| `position` | object |  |
| `status` | string |  |

## Native endpoint

Through the native Zeplin API, this operation is `GET /projects/{project_id}/screens/{screen_id}/notes` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-screen-notes.md) for the provider-specific parameters and requirements.

