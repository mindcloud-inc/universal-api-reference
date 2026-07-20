# Agility CMS Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Agility CMS expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/list-categories-fetch?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Agility CMS actions that support pagination

- [List Categories (Fetch)](actions/list-categories-fetch.md)
- [List Categories (Preview)](actions/list-categories-preview.md)
- [List Content Items (Fetch)](actions/list-content-items-fetch.md)
- [List Content Items (Preview)](actions/list-content-items-preview.md)
- [List Content Items V1 (Fetch)](actions/list-content-items-v1-fetch.md)
- [List Content Items V1 (Preview)](actions/list-content-items-v1-preview.md)
- [List Posts (Fetch)](actions/list-posts-fetch.md)
- [List Posts (Preview)](actions/list-posts-preview.md)
