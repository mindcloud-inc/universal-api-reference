# KYVE Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model KYVE expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/count-stakers-by-pool?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## KYVE actions that support pagination

- [Count Stakers By Pool](actions/count-stakers-by-pool.md)
- [List Finalized Bundles](actions/list-finalized-bundles.md)
- [List Funders](actions/list-funders.md)
- [List Fundings By Funder](actions/list-fundings-by-funder.md)
- [List Fundings By Pool](actions/list-fundings-by-pool.md)
- [List Liquid Validators](actions/list-liquid-validators.md)
- [List Pools](actions/list-pools.md)
- [List Stakers](actions/list-stakers.md)
- [List Tokenize Share Records](actions/list-tokenize-share-records.md)
