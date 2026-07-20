# Apple News and Music Universal API Examples

These examples use the MindCloud API key and Apple News and Music connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Lookup Catalog Item by iTunes ID

Retrieves a catalog item from Apple's catalog by iTunes ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appleNewsAndMusic/latest/actions/lookup-catalog-item-by-itunes-id?connectionId=$CONNECTION_ID&id=e.g.%20909253" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "e.g. 909253"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appleNewsAndMusic/latest/actions/lookup-catalog-item-by-itunes-id?${params}`, {
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
      "amgArtistId": 1,
      "artistId": 1,
      "artistLinkUrl": "https://example.com",
      "artistName": "Ava Chen",
      "artworkUrl100": "https://example.com",
      "averageUserRating": 1,
      "collectionId": 1,
      "collectionName": "Ava Chen",
      "collectionPrice": 1,
      "collectionViewUrl": "https://example.com",
      "currency": "string",
      "description": "string",
      "formattedPrice": "string",
      "kind": "string",
      "primaryGenreName": "Ava Chen",
      "releaseDate": "2026-05-07T12:00:00.000Z",
      "trackId": 1,
      "trackName": "Ava Chen",
      "trackPrice": 1,
      "trackViewUrl": "https://example.com",
      "userRatingCount": 1,
      "wrapperType": "string"
    }
  ],
  "meta": {}
}
```

See the full [Lookup Catalog Item by iTunes ID action reference](actions/lookup-catalog-item-by-itunes-id.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/appleNewsAndMusic/latest/actions/lookup-catalog-item-by-itunes-id).
