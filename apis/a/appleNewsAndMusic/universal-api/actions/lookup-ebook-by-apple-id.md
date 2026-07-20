# Apple News and Music: Lookup Ebook by Apple ID

Retrieves an ebook from Apple's catalog by Apple ID.

```
GET https://connect.mindcloud.co/v1/universal/appleNewsAndMusic/latest/actions/lookup-ebook-by-apple-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apple News and Music `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appleNewsAndMusic/latest/actions/lookup-ebook-by-apple-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appleNewsAndMusic/latest/actions/lookup-ebook-by-apple-id?${params}`, {
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
| `id` | string | yes | Apple ebook identifier to look up. |
| `entity` | string | no | Fixed Apple lookup entity. Default: `ebook`. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amgArtistId` | number | AllMusic artist identifier when Apple includes it. |
| `artistId` | number | Apple artist identifier. |
| `artistLinkUrl` | string | Apple URL for the artist page. |
| `artistName` | string | Artist or creator name. |
| `artworkUrl100` | string | 100x100 artwork image URL. |
| `averageUserRating` | number | Average user rating when available. |
| `collectionId` | number | Apple collection identifier. |
| `collectionName` | string | Album, playlist, or collection title. |
| `collectionPrice` | number | Collection price when Apple includes one. |
| `collectionViewUrl` | string | Apple URL for the collection page. |
| `currency` | string | Currency code for catalog pricing. |
| `description` | string | Item description or summary text. |
| `formattedPrice` | string | Formatted price label for books and similar items. |
| `kind` | string | Apple catalog item kind such as song, album, podcast, or ebook. |
| `primaryGenreName` | string | Primary Apple genre name. |
| `releaseDate` | date | Release or publish date. |
| `trackId` | number | Apple track or item identifier. |
| `trackName` | string | Track, episode, or item title. |
| `trackPrice` | number | Track price when Apple includes one. |
| `trackViewUrl` | string | Apple URL for the specific item page. |
| `userRatingCount` | number | Number of ratings when available. |
| `wrapperType` | string | Apple wrapper type for the returned catalog item. |

## Native endpoint

Through the native Apple News and Music API, this operation is `GET https://itunes.apple.com/lookup` (base URL `https://itunes.apple.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-ebook-by-apple-id.md) for the provider-specific parameters and requirements.

