# Library of Congress Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Library of Congress expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/libraryOfCongress/latest/actions/get-collection-results?connectionId=$CONNECTION_ID&limit=25&offset=0&collectionSlug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Library of Congress actions that support pagination

- [Get Collection Results](actions/get-collection-results.md)
- [List Collections](actions/list-collections.md)
- [Search All Content](actions/search-all-content.md)
- [Search Audio Recordings](actions/search-audio-recordings.md)
- [Search Books](actions/search-books.md)
- [Search Collection Items](actions/search-collection-items.md)
- [Search Film and Videos](actions/search-film-and-videos.md)
- [Search Manuscripts](actions/search-manuscripts.md)
- [Search Maps](actions/search-maps.md)
- [Search Newspapers](actions/search-newspapers.md)
- [Search Notated Music](actions/search-notated-music.md)
- [Search Periodicals](actions/search-periodicals.md)
- [Search Personal Narratives](actions/search-personal-narratives.md)
- [Search Photos](actions/search-photos.md)
- [Search Software and E-Resources](actions/search-software-and-e-resources.md)
- [Search Sound Recordings](actions/search-sound-recordings.md)
- [Search Web Archives](actions/search-web-archives.md)
- [Search 3D Objects](actions/search3d-objects.md)
