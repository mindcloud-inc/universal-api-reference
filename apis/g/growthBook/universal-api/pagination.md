# GrowthBook Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model GrowthBook expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/get-feature-revisions?connectionId=$CONNECTION_ID&limit=25&offset=0&id=prj_19g6smo332up7" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## GrowthBook actions that support pagination

- [List revisions for a feature](actions/get-feature-revisions.md)
- [Get list of all code references for the current organization](actions/list-code-refs.md)
- [Get all data sources](actions/list-data-sources.md)
- [Get all dimensions](actions/list-dimensions.md)
- [Get all experiments](actions/list-experiments.md)
- [Get all fact metrics](actions/list-fact-metrics.md)
- [Get all filters for a fact table](actions/list-fact-table-filters.md)
- [Get all fact tables](actions/list-fact-tables.md)
- [Get all features](actions/list-features.md)
- [Get all organization members](actions/list-members.md)
- [Get all metrics](actions/list-metrics.md)
- [Get all organizations (only for super admins on multi-org Enterprise Plan only)](actions/list-organizations.md)
- [Get all projects](actions/list-projects.md)
- [Get all rampSchedules](actions/list-ramp-schedules.md)
- [List feature revisions](actions/list-revisions.md)
- [Get all saved group](actions/list-saved-groups.md)
- [Get all sdk connections](actions/list-sdk-connections.md)
- [Get all segments](actions/list-segments.md)
