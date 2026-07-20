# Reflect: List Books

Retrieves books from a graph in Reflect.

```
GET https://connect.mindcloud.co/v1/universal/reflect/latest/actions/list-books
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reflect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reflect/latest/actions/list-books?connectionId=$CONNECTION_ID&graphId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "graphId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reflect/latest/actions/list-books?${params}`, {
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
| `graphId` | list<string> | yes | Your graph identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asin": "string",
      "authors": [
        "string"
      ],
      "id": "string",
      "notes": [
        {}
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asin` | string |  |
| `authors` | array<string> |  |
| `id` | string |  |
| `notes` | array<object> |  |
| `title` | string |  |

## Native endpoint

Through the native Reflect API, this operation is `GET /graphs/:graphId/books` (base URL `https://reflect.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-books.md) for the provider-specific parameters and requirements.

