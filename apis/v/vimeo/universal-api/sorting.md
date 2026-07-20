# Vimeo Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Vimeo expects, and each action page lists the fields available to sort.

## Vimeo actions that support sorting

- [List Available Video Showcases](actions/list-available-video-showcases.md)
- [List Channel Videos](actions/list-channel-videos.md)
- [List Channels](actions/list-channels.md)
- [List Project Videos](actions/list-project-videos.md)
- [List Projects](actions/list-projects.md)
- [List Showcase Videos](actions/list-showcase-videos.md)
- [List Showcases](actions/list-showcases.md)
- [List User Videos](actions/list-user-videos.md)
- [List Videos with Tag](actions/list-videos-with-tag.md)
- [Search Videos](actions/search-videos.md)
