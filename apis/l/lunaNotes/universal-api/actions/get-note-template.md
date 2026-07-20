# LunaNotes: Get Note Template

Retrieves a note template from LunaNotes.

```
GET https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/get-note-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LunaNotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/get-note-template?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/get-note-template?${params}`, {
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
| `id` | string | yes | The LunaNotes note template ID. |
| `include` | string | no | Include the related system template in the response |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorId": "string",
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "json": {},
      "systemTemplate": {},
      "systemTemplateId": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorId` | string | Owner user ID |
| `content` | string | Plain text template content |
| `createdAt` | date | Timestamp when the template was created |
| `id` | string | Unique identifier for the note template |
| `json` | object | Tiptap JSON content structure |
| `systemTemplate` | object | Source system template |
| `systemTemplateId` | string | Source system template ID |
| `title` | string | Template title |
| `updatedAt` | date | Timestamp when the template was last updated |

## Native endpoint

Through the native LunaNotes API, this operation is `GET /v1/note-templates/:id` (base URL `https://api.lunanotes.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-note-template.md) for the provider-specific parameters and requirements.

