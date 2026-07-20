# Flotiq: List Content Types

Retrieves content types from your Flotiq project.

```
GET https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/list-content-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flotiq `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/list-content-types?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/list-content-types?${params}`, {
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
| `name` | string | no | Filter content types by name. |

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
| `autoSave` | boolean | Whether autosave is enabled for the content type. |
| `createdAt` | date | The creation timestamp. |
| `deletedAt` | date | The deletion timestamp, when present. |
| `draftPublic` | boolean | Whether Draft & Public is enabled for the content type. |
| `featuredImage` | array<object> | The featured image references. |
| `id` | string | The Flotiq content type ID. |
| `internal` | boolean | Whether the content type is internal to Flotiq. |
| `label` | string | The human-readable content type label. |
| `metaDefinition` | object | The Flotiq meta-definition for the content type. |
| `name` | string | The content type name. |
| `schemaDefinition` | object | The JSON schema definition for the content type. |
| `updatedAt` | date | The last update timestamp. |

## Native endpoint

Through the native Flotiq API, this operation is `GET /internal/contenttype` (base URL `https://api.flotiq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-content-types.md) for the provider-specific parameters and requirements.

