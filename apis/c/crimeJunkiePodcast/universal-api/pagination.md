# Crime Junkie Podcast Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Crime Junkie Podcast expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crimeJunkiePodcast/latest/actions/list-attachment-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Crime Junkie Podcast actions that support pagination

- [List Attachment Categories](actions/list-attachment-categories.md)
- [List Authors](actions/list-authors.md)
- [List Blocks](actions/list-blocks.md)
- [List Categories](actions/list-categories.md)
- [List Comments](actions/list-comments.md)
- [List Dipi Content Categories](actions/list-dipi-content-categories.md)
- [List Dipi Media Categories](actions/list-dipi-media-categories.md)
- [List Fan Club Episodes](actions/list-fan-club-episodes.md)
- [List Fan Club Tiers](actions/list-fan-club-tiers.md)
- [List Good Tags](actions/list-good-tags.md)
- [List Media](actions/list-media.md)
- [List Navigation Menus](actions/list-navigation-menus.md)
- [List Pages](actions/list-pages.md)
- [List Pattern Categories](actions/list-pattern-categories.md)
- [List Popup Makers](actions/list-popup-makers.md)
- [List Posts](actions/list-posts.md)
- [List Project Categories](actions/list-project-categories.md)
- [List Project Tags](actions/list-project-tags.md)
- [List Projects](actions/list-projects.md)
- [List Pruppet Categories](actions/list-pruppet-categories.md)
- [List Pruppets](actions/list-pruppets.md)
- [List Tags](actions/list-tags.md)
- [List The Goods](actions/list-the-goods.md)
- [Search Content](actions/search-content.md)
