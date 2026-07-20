# Brasil API: Get Book by ISBN

Retrieves book details from Brasil API by ISBN.

```
GET https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-book-by-isbn
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brasil API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-book-by-isbn?connectionId=$CONNECTION_ID&isbn=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "isbn": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-book-by-isbn?${params}`, {
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
| `isbn` | string | yes | The ISBN code to look up. |
| `providers` | string | no | Optional comma-separated ISBN providers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authors": [
        "string"
      ],
      "cover_url": "https://example.com",
      "dimensions": {},
      "format": "string",
      "isbn": "string",
      "location": "string",
      "page_count": 1,
      "provider": "string",
      "publisher": "string",
      "retail_price": {},
      "subjects": [
        "string"
      ],
      "subtitle": "string",
      "synopsis": "string",
      "title": "string",
      "year": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authors` | array<string> |  |
| `cover_url` | string |  |
| `dimensions` | object |  |
| `format` | string |  |
| `isbn` | string |  |
| `location` | string |  |
| `page_count` | number |  |
| `provider` | string |  |
| `publisher` | string |  |
| `retail_price` | object |  |
| `subjects` | array<string> |  |
| `subtitle` | string |  |
| `synopsis` | string |  |
| `title` | string |  |
| `year` | number |  |

## Native endpoint

Through the native Brasil API API, this operation is `GET /isbn/v1/{isbn}` (base URL `https://brasilapi.com.br/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-book-by-isbn.md) for the provider-specific parameters and requirements.

