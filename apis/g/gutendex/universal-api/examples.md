# Gutendex Universal API Examples

These examples use the MindCloud API key and Gutendex connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Book

Retrieves book details from Gutendex.

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

Example response:

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

See the full [Get Book action reference](actions/get-book.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gutendex/latest/actions/get-book).
