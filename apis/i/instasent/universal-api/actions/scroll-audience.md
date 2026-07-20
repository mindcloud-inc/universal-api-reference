# Instasent: Scroll Audience



```
GET https://connect.mindcloud.co/v1/universal/instasent/latest/actions/scroll-audience
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instasent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instasent/latest/actions/scroll-audience?connectionId=$CONNECTION_ID&project=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instasent/latest/actions/scroll-audience?${params}`, {
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
| `project` | string | yes | Instasent project uid. Use the uid value from List Projects, not the internal project id. |
| `root` | object | no | Audience filter tree to scroll. |
| `limit` | number | no | Maximum number of results to return per page. |
| `cursor` | string | no | Pagination cursor from the previous scroll response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entities": [
        {
          "attributesData": {},
          "createdAt": "string",
          "deletedAt": "string",
          "id": "string",
          "indexedAt": "string",
          "updatedAt": "string"
        }
      ],
      "metadata": {
        "cursor": "string",
        "limit": 1,
        "totalHits": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entities[].attributesData` | object | Audience contact attribute payload |
| `entities[].createdAt` | string | Audience contact creation timestamp |
| `entities[].deletedAt` | string | Audience contact deletion timestamp when soft-deleted |
| `entities[].id` | string | Audience contact identifier |
| `entities[].indexedAt` | string | Audience contact index timestamp |
| `entities[].updatedAt` | string | Audience contact last update timestamp |
| `metadata.cursor` | string | Cursor token for the next page, or null when no more results are available |
| `metadata.limit` | number | Maximum number of contacts returned in this page |
| `metadata.totalHits` | number | Total number of matching audience contacts |

## Native endpoint

Through the native Instasent API, this operation is `POST /project/:project/audience/scroll` (base URL `https://api.instasent.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scroll-audience.md) for the provider-specific parameters and requirements.

