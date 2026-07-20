# Incontrol: Get Case Note

Retrieves details for a case note from Incontrol.

```
GET https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/get-case-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Incontrol `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/get-case-note?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/get-case-note?${params}`, {
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
| `id` | string | yes | The case note ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "case": {},
      "created": "2026-05-07T12:00:00.000Z",
      "hasFiles": true,
      "id": "string",
      "text": "string",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `case` | object |  |
| `created` | date |  |
| `hasFiles` | boolean |  |
| `id` | string |  |
| `text` | string |  |
| `user` | object |  |

## Native endpoint

Through the native Incontrol API, this operation is `GET /api/v1/casenote/{{id}}` (base URL `https://portal.incontrol.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-case-note.md) for the provider-specific parameters and requirements.

