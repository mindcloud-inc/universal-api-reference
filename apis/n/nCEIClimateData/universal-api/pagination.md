# NCEI Climate Data Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model NCEI Climate Data expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nCEIClimateData/latest/actions/list-climate-data?connectionId=$CONNECTION_ID&limit=25&offset=0&datasetid=GHCND&startdate=2010-05-01&enddate=2010-05-01" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## NCEI Climate Data actions that support pagination

- [List Climate Data](actions/list-climate-data.md)
- [List Data Categories](actions/list-data-categories.md)
- [List Data Types](actions/list-data-types.md)
- [List Datasets](actions/list-datasets.md)
- [List Location Categories](actions/list-location-categories.md)
- [List Locations](actions/list-locations.md)
- [List Stations](actions/list-stations.md)
