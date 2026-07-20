# Gutendex: Get Book

Retrieves book details from Gutendex.

```
GET https://connect.mindcloud.co/v1/universal/gutendex/latest/actions/get-book
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gutendex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gutendex/latest/actions/get-book?connectionId=$CONNECTION_ID&bookId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gutendex/latest/actions/get-book?${params}`, {
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
| `bookId` | number | yes | Project Gutenberg book ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authors": [
        {}
      ],
      "bookshelves": [
        "string"
      ],
      "copyright": true,
      "download_count": 1,
      "formats": {},
      "id": 1,
      "languages": [
        "string"
      ],
      "media_type": "string",
      "subjects": [
        "string"
      ],
      "summaries": [
        "string"
      ],
      "title": "string",
      "translators": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authors` | array<object> |  |
| `bookshelves` | array<string> |  |
| `copyright` | boolean |  |
| `download_count` | number |  |
| `formats` | object |  |
| `id` | number |  |
| `languages` | array<string> |  |
| `media_type` | string |  |
| `subjects` | array<string> |  |
| `summaries` | array<string> |  |
| `title` | string |  |
| `translators` | array<object> |  |

## Native endpoint

Through the native Gutendex API, this operation is `GET /books/:bookId/` (base URL `https://gutendex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-book.md) for the provider-specific parameters and requirements.

