# Zeplin: List Screen Annotation Note Types

Retrieves screen annotation note types from Zeplin.

```
GET https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-screen-annotation-note-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-screen-annotation-note-types?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-screen-annotation-note-types?${params}`, {
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
      "color": {},
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | object |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Zeplin API, this operation is `GET /projects/{project_id}/annotations/note_types` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-screen-annotation-note-types.md) for the provider-specific parameters and requirements.

