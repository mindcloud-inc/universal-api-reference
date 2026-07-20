# Flotiq: Get Content Type

Retrieves a content type from your Flotiq project.

```
GET https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/get-content-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flotiq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/get-content-type?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/get-content-type?${params}`, {
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
| `id` | string | yes | The Flotiq content type ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autoSave": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "draftPublic": true,
      "featuredImage": [
        {}
      ],
      "id": "string",
      "internal": true,
      "label": "string",
      "metaDefinition": {},
      "name": "Ava Chen",
      "schemaDefinition": {},
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoSave` | boolean |  |
| `createdAt` | date |  |
| `deletedAt` | date |  |
| `draftPublic` | boolean |  |
| `featuredImage` | array<object> |  |
| `id` | string |  |
| `internal` | boolean |  |
| `label` | string |  |
| `metaDefinition` | object |  |
| `name` | string |  |
| `schemaDefinition` | object |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Flotiq API, this operation is `GET /internal/contenttype/{{id}}` (base URL `https://api.flotiq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-content-type.md) for the provider-specific parameters and requirements.

