# Readwise: Get Book Tag

Retrieves a tag from a Readwise book.

```
GET https://connect.mindcloud.co/v1/universal/readwise/latest/actions/get-book-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Readwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/readwise/latest/actions/get-book-tag?connectionId=$CONNECTION_ID&bookId=1&tagId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookId": "1",
  "tagId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/readwise/latest/actions/get-book-tag?${params}`, {
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
| `bookId` | number | yes | Readwise book ID. |
| `tagId` | number | yes | Readwise tag ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Readwise API, this operation is `GET /api/v2/books/:bookId/tags/:tagId` (base URL `https://readwise.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-book-tag.md) for the provider-specific parameters and requirements.

