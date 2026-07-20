# Veterans Affairs Facilities Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Veterans Affairs Facilities expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veteransAffairsFacilities/latest/actions/find-nearby-facilities-by-coordinates?connectionId=$CONNECTION_ID&limit=25&offset=0&lat=1&long=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Veterans Affairs Facilities actions that support pagination

- [Find Nearby Facilities by Coordinates](actions/find-nearby-facilities-by-coordinates.md)
- [Search Facilities by Bounding Box](actions/search-facilities-by-bounding-box.md)
- [Search Facilities by Coordinates](actions/search-facilities-by-coordinates.md)
- [Search Facilities by State](actions/search-facilities-by-state.md)
- [Search Facilities by ZIP Code](actions/search-facilities-by-zip-code.md)
