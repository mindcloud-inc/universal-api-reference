# HigherGov Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format HigherGov expects, and each action page lists the fields available to sort.

## HigherGov actions that support sorting

- [List Awardees](actions/list-awardees.md)
- [List Contract Vehicles](actions/list-contract-vehicles.md)
- [List Federal Contracts](actions/list-federal-contracts.md)
- [List Federal Grants](actions/list-federal-grants.md)
- [List IDV Awards](actions/list-idv-awards.md)
- [List NAICS Codes](actions/list-naics-codes.md)
- [List NSNs](actions/list-nsns.md)
- [List Opportunities](actions/list-opportunities.md)
- [List Opportunity Documents](actions/list-opportunity-documents.md)
- [List People](actions/list-people.md)
- [List State And Local Contracts](actions/list-state-and-local-contracts.md)
- [List Subcontracts](actions/list-subcontracts.md)
- [List Subgrants](actions/list-subgrants.md)
