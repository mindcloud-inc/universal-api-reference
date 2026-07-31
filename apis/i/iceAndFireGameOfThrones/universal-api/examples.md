# Ice and Fire (Game of Thrones) Universal API Examples

These examples use the MindCloud API key and Ice and Fire (Game of Thrones) connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Book



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

Example response:

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

See the full [Get Book action reference](actions/get-book.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iceAndFireGameOfThrones/latest/actions/get-book).
