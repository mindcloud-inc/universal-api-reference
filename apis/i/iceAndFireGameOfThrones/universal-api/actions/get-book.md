# Ice and Fire (Game of Thrones): Get Book



```
GET https://connect.mindcloud.co/v1/universal/iceAndFireGameOfThrones/latest/actions/get-book
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ice and Fire (Game of Thrones) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iceAndFireGameOfThrones/latest/actions/get-book?connectionId=$CONNECTION_ID&bookId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iceAndFireGameOfThrones/latest/actions/get-book?${params}`, {
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
| `bookId` | number | yes | The numeric ID of the book to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authors": [
        "string"
      ],
      "characters": [
        "string"
      ],
      "country": "string",
      "isbn": "string",
      "mediaType": "string",
      "name": "Ava Chen",
      "numberOfPages": 1,
      "povCharacters": [
        "string"
      ],
      "publisher": "string",
      "released": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authors` | array<string> |  |
| `characters` | array<string> |  |
| `country` | string |  |
| `isbn` | string |  |
| `mediaType` | string |  |
| `name` | string |  |
| `numberOfPages` | number |  |
| `povCharacters` | array<string> |  |
| `publisher` | string |  |
| `released` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Ice and Fire (Game of Thrones) API, this operation is `GET /books/:bookId` (base URL `https://anapioficeandfire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-book.md) for the provider-specific parameters and requirements.

