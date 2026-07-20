# HigherGov Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model HigherGov expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-agencies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## HigherGov actions that support pagination

- [List Agencies](actions/list-agencies.md)
- [List Awardee Partnerships](actions/list-awardee-partnerships.md)
- [List Awardees](actions/list-awardees.md)
- [List Contract Vehicles](actions/list-contract-vehicles.md)
- [List Federal Contracts](actions/list-federal-contracts.md)
- [List Federal Grants](actions/list-federal-grants.md)
- [List Grant Programs](actions/list-grant-programs.md)
- [List IDV Awards](actions/list-idv-awards.md)
- [List Mentor Protege Relationships](actions/list-mentor-protege-relationships.md)
- [List NAICS Codes](actions/list-naics-codes.md)
- [List NSNs](actions/list-nsns.md)
- [List Opportunities](actions/list-opportunities.md)
- [List Opportunity Documents](actions/list-opportunity-documents.md)
- [List People](actions/list-people.md)
- [List PSC Codes](actions/list-psc-codes.md)
- [List Pursuits](actions/list-pursuits.md)
- [List State And Local Contracts](actions/list-state-and-local-contracts.md)
- [List Subcontracts](actions/list-subcontracts.md)
- [List Subgrants](actions/list-subgrants.md)
