# Pixabay Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Pixabay expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixabay/latest/actions/search-animal-images?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Pixabay actions that support pagination

- [Search Animal Images](actions/search-animal-images.md)
- [Search Animal Videos](actions/search-animal-videos.md)
- [Search Animations](actions/search-animations.md)
- [Search Background Images](actions/search-background-images.md)
- [Search Background Videos](actions/search-background-videos.md)
- [Search Building Images](actions/search-building-images.md)
- [Search Building Videos](actions/search-building-videos.md)
- [Search Business Images](actions/search-business-images.md)
- [Search Business Videos](actions/search-business-videos.md)
- [Search Computer Images](actions/search-computer-images.md)
- [Search Computer Videos](actions/search-computer-videos.md)
- [Search Editor's Choice Images](actions/search-editors-choice-images.md)
- [Search Editor's Choice Videos](actions/search-editors-choice-videos.md)
- [Search Education Images](actions/search-education-images.md)
- [Search Education Videos](actions/search-education-videos.md)
- [Search Fashion Images](actions/search-fashion-images.md)
- [Search Fashion Videos](actions/search-fashion-videos.md)
- [Search Feeling Images](actions/search-feeling-images.md)
- [Search Feeling Videos](actions/search-feeling-videos.md)
- [Search Films](actions/search-films.md)
- [Search Food Images](actions/search-food-images.md)
- [Search Food Videos](actions/search-food-videos.md)
- [Search Health Images](actions/search-health-images.md)
- [Search Health Videos](actions/search-health-videos.md)
- [Search Horizontal Images](actions/search-horizontal-images.md)
- [Search Illustrations](actions/search-illustrations.md)
- [Search Images](actions/search-images.md)
- [Search Industry Images](actions/search-industry-images.md)
- [Search Industry Videos](actions/search-industry-videos.md)
- [Search Latest Images](actions/search-latest-images.md)
- [Search Latest Videos](actions/search-latest-videos.md)
- [Search Music Images](actions/search-music-images.md)
- [Search Music Videos](actions/search-music-videos.md)
- [Search Nature Images](actions/search-nature-images.md)
- [Search Nature Videos](actions/search-nature-videos.md)
- [Search People Images](actions/search-people-images.md)
- [Search People Videos](actions/search-people-videos.md)
- [Search Photos](actions/search-photos.md)
- [Search Place Images](actions/search-place-images.md)
- [Search Place Videos](actions/search-place-videos.md)
- [Search Religion Images](actions/search-religion-images.md)
- [Search Religion Videos](actions/search-religion-videos.md)
- [Search Safe Images](actions/search-safe-images.md)
- [Search Safe Videos](actions/search-safe-videos.md)
- [Search Science Images](actions/search-science-images.md)
- [Search Science Videos](actions/search-science-videos.md)
- [Search Sports Images](actions/search-sports-images.md)
- [Search Sports Videos](actions/search-sports-videos.md)
- [Search Transportation Images](actions/search-transportation-images.md)
- [Search Transportation Videos](actions/search-transportation-videos.md)
- [Search Travel Images](actions/search-travel-images.md)
- [Search Travel Videos](actions/search-travel-videos.md)
- [Search Vectors](actions/search-vectors.md)
- [Search Vertical Images](actions/search-vertical-images.md)
- [Search Videos](actions/search-videos.md)
