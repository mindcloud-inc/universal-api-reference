# Readwise: Remove Book Tag

Deletes a tag from a Readwise book.

```
DELETE https://connect.mindcloud.co/v1/universal/readwise/latest/actions/remove-book-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Readwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/readwise/latest/actions/remove-book-tag?connectionId=$CONNECTION_ID&bookId=1&tagId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookId": "1",
  "tagId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/readwise/latest/actions/remove-book-tag?${params}`, {
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
| `bookId` | number | yes | The Readwise book ID that owns the tag. |
| `tagId` | number | yes | The Readwise tag ID to remove. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Readwise API, this operation is `DELETE /api/v2/books/:bookId/tags/:tagId` (base URL `https://readwise.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-book-tag.md) for the provider-specific parameters and requirements.

