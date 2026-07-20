# Mem: List Collections

Retrieves collections from Mem.

```
GET https://connect.mindcloud.co/v1/universal/mem/latest/actions/list-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mem `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mem/latest/actions/list-collections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mem/latest/actions/list-collections?${params}`, {
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
| `orderBy` | string | no | Optional collection ordering. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPage": "string",
      "requestId": "string",
      "results": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "id": "string",
          "title": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextPage` | string | Pagination token for the next page of collections. |
| `requestId` | string | Mem request identifier. |
| `results[].createdAt` | date | Collection creation timestamp. |
| `results[].description` | string | Collection description. |
| `results[].id` | string | Mem collection identifier. |
| `results[].title` | string | Collection title. |
| `results[].updatedAt` | date | Collection last update timestamp. |

## Native endpoint

Through the native Mem API, this operation is `GET /v2/collections` (base URL `https://api.mem.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-collections.md) for the provider-specific parameters and requirements.

