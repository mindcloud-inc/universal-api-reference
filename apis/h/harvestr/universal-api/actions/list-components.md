# Harvestr.io: List Components



```
GET https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/list-components
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvestr.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/list-components?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/list-components?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createdBefore` | date | no | Filter items created before this date (ISO 8601 format) |
| `createdAfter` | date | no | Filter items created after this date (ISO 8601 format) |
| `updatedBefore` | date | no | Filter items updated before this date (ISO 8601 format) |
| `updatedAfter` | date | no | Filter items updated after this date (ISO 8601 format) |
| `parentId` | string | no | Filter components by parent component ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "parentId": "string",
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
| `clientId` | string | Client identifier |
| `createdAt` | date | Creation date of the component |
| `description` | string | Description of the component |
| `id` | string | Unique identifier of the component |
| `parentId` | string | Parent component identifier for hierarchical structure |
| `title` | string | Title of the component |
| `updatedAt` | date | Last update date of the component |

## Native endpoint

Through the native Harvestr.io API, this operation is `GET /component` (base URL `https://rest.harvestr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-components.md) for the provider-specific parameters and requirements.

