# Zeplin: Get Screen Note

Retrieves a screen note from Zeplin.

```
GET https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/get-screen-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/get-screen-note?connectionId=$CONNECTION_ID&projectId=string&screenId=string&noteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "screenId": "string",
  "noteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/get-screen-note?${params}`, {
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
| `noteId` | string | yes | Screen note id |

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

Through the native Zeplin API, this operation is `GET /projects/{project_id}/screens/{screen_id}/notes/{note_id}` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-screen-note.md) for the provider-specific parameters and requirements.

