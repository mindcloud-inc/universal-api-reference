# Flotiq: Create Content Type

Creates a new content type in Flotiq.

```
POST https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/create-content-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flotiq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/create-content-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/create-content-type', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | The content type definition payload. |

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

Through the native Flotiq API, this operation is `POST /internal/contenttype` (base URL `https://api.flotiq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-content-type.md) for the provider-specific parameters and requirements.

