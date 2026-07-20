# Sellfy Universal API Examples

These examples use the MindCloud API key and Sellfy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get oEmbed

Retrieves oEmbed data from Sellfy for a store or product URL.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sellfy/latest/actions/get-oembed?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fdemo.sellfy.store%2Fp%2Fbottle-mockup%2F" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://demo.sellfy.store/p/bottle-mockup/"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sellfy/latest/actions/get-oembed?${params}`, {
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
      "authorName": "Ava Chen",
      "authorUrl": "https://example.com",
      "html": "string",
      "id": "string",
      "providerName": "Ava Chen",
      "providerUrl": "https://example.com",
      "thumbnailHeight": 1,
      "thumbnailUrl": "https://example.com",
      "thumbnailWidth": 1,
      "title": "string",
      "type": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get oEmbed action reference](actions/get-oembed.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sellfy/latest/actions/get-oembed).
