# RollWorks: Native API Reference

A consolidated summary of RollWorks's API configuration and 57 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.nextroll.com/guides/get-started-rollworks.html
- **API base URL:** `https://services.adroll.com`

## Authentication

### API Key

Connect RollWorks using a NextRoll personal access token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://apidocs.nextroll.com/guides/api-key-migration.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (57 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Accept Segment Sharing Invitation](actions/accept-segment-sharing-invitation.md) | `POST /audience/v1/sharing/segment` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#post--audience-v1-sharing-segment) |
| [Bulk Create Or Update Segments by Bulk Route](actions/bulk-create-or-update-segments-by-bulk-route.md) | `POST /audience/v1/segments/bulk` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#post--audience-v1-segments-bulk) |
| [Bulk Create Or Update Segments by Put Route](actions/bulk-create-or-update-segments-by-put-route.md) | `POST /audience/v1/segments_bulk/put` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#post--audience-v1-segments_bulk-put) |
| [Create ICP by Advertisable EID](actions/create-icp-by-advertisable-eid.md) | `POST /audience/v1/ideal_customer_profile` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#post--audience-v1-ideal_customer_profile) |
| [Create Segment](actions/create-segment.md) | `POST /audience/v1/segments` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#post--audience-v1-segments) |
| [Create Segment Sharing Invitation](actions/create-segment-sharing-invitation.md) | `POST /audience/v1/sharing/invitation` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#post--audience-v1-sharing-invitation) |
| [Create Target Accounts List](actions/create-target-accounts-list.md) | `POST /audience/v1/target_accounts` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#post--audience-v1-target_accounts) |
| [Create Target Accounts Tier](actions/create-target-accounts-tier.md) | `POST /audience/v1/target_accounts/:tal_eid/tiers` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#post--audience-v1-target_accounts-(tal_eid)-tiers) |
| [Delete ICP by ICP EID and Advertisable EID](actions/delete-icp-by-icp-eid-and-advertisable-eid.md) | `DELETE /audience/v1/ideal_customer_profile/:icp_eid` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#delete--audience-v1-ideal_customer_profile-(icp_eid)) |
| [Delete Mirror Segment](actions/delete-mirror-segment.md) | `DELETE /audience/v1/sharing/segment` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#delete--audience-v1-sharing-segment) |
| [Delete Segment](actions/delete-segment.md) | `DELETE /audience/v1/segments/:segment_id` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#delete--audience-v1-segments-(segment_id)) |
| [Delete Target Accounts List](actions/delete-target-accounts-list.md) | `DELETE /audience/v1/target_accounts/:tal_eid` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#delete--audience-v1-target_accounts-(tal_eid)) |
| [Delete Target Accounts List Items by Delete Route](actions/delete-target-accounts-list-items-by-delete-route.md) | `DELETE /audience/v1/target_accounts/:tal_eid/tiers/:ta_tier_eid/items` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#delete--audience-v1-target_accounts-(tal_eid)-tiers-(ta_tier_eid)-items) |
| [Delete Target Accounts List Items by Post Delete Route](actions/delete-target-accounts-list-items-by-post-delete-route.md) | `POST /audience/v1/target_accounts/:tal_eid/tiers/:ta_tier_eid/items/delete` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#post--audience-v1-target_accounts-(tal_eid)-tiers-(ta_tier_eid)-items-delete) |
| [Delete Target Accounts Tier](actions/delete-target-accounts-tier.md) | `DELETE /audience/v1/target_accounts/:tal_eid/tiers/:ta_tier_eid` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#delete--audience-v1-target_accounts-(tal_eid)-tiers-(ta_tier_eid)) |
| [Estimate Composite Segment Size](actions/estimate-composite-segment-size.md) | `GET /user-lists/api/v1/userlists/audience_preview` | [docs](https://apidocs.nextroll.com/user-lists-api/reference.html#get--user-lists-api-v1-userlists-audience_preview) |
| [Execute GraphQL queries](actions/execute-graphql-queries.md) | `POST /reporting/api/v1/query` | [docs](https://apidocs.nextroll.com/graphql-reporting-api/reference.html#post--reporting-api-v1-query) |
| [Get CDP Plus User List Sizes by Segment and Date](actions/get-cdp-plus-user-list-sizes-by-segment-and-date.md) | `GET /user-lists/api/v1/userlists/segment/cdp_plus` | [docs](https://apidocs.nextroll.com/user-lists-api/reference.html#get--user-lists-api-v1-userlists-segment-cdp_plus) |
| [Get Domain References](actions/get-domain-references.md) | `POST /audience/v1/target_accounts/domain_references` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#post--audience-v1-target_accounts-domain_references) |
| [Get Exact User Counts by Date and Metric](actions/get-exact-user-counts-by-date-and-metric.md) | `GET /user-lists/api/v1/userlists/segment/exact` | [docs](https://apidocs.nextroll.com/user-lists-api/reference.html#get--user-lists-api-v1-userlists-segment-exact) |
| [Get ICP by ICP EID and Advertisable EID](actions/get-icp-by-icp-eid-and-advertisable-eid.md) | `GET /audience/v1/ideal_customer_profile/:icp_eid` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#get--audience-v1-ideal_customer_profile-(icp_eid)) |
| [Get Segment](actions/get-segment.md) | `GET /audience/v1/segments/:segment_id` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#get--audience-v1-segments-(segment_id)) |
| [Get Source Segment for Sharing Invitation](actions/get-source-segment-for-sharing-invitation.md) | `GET /audience/v1/sharing/get_source_segment` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#get--audience-v1-sharing-get_source_segment) |
| [Get Target Accounts List](actions/get-target-accounts-list.md) | `GET /audience/v1/target_accounts/:tal_eid` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#get--audience-v1-target_accounts-(tal_eid)) |
| [Get Target Accounts Tier](actions/get-target-accounts-tier.md) | `GET /audience/v1/target_accounts/:tal_eid/tiers/:ta_tier_eid` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#get--audience-v1-target_accounts-(tal_eid)-tiers-(ta_tier_eid)) |
| [Get User Attribute Counts by Name and Value](actions/get-user-attribute-counts-by-name-and-value.md) | `POST /audience/v1/user_attribute_counts` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#post--audience-v1-user_attribute_counts) |
| [Get User List Sizes by Ad and Date](actions/get-user-list-sizes-by-ad-and-date.md) | `GET /user-lists/api/v1/userlists/ad` | [docs](https://apidocs.nextroll.com/user-lists-api/reference.html#get--user-lists-api-v1-userlists-ad) |
| [Get User List Sizes by Ad Group and Date](actions/get-user-list-sizes-by-ad-group-and-date.md) | `GET /user-lists/api/v1/userlists/adgroup` | [docs](https://apidocs.nextroll.com/user-lists-api/reference.html#get--user-lists-api-v1-userlists-adgroup) |
| [Get User List Sizes by Advertisable and Date](actions/get-user-list-sizes-by-advertisable-and-date.md) | `GET /user-lists/api/v1/userlists/advertisable` | [docs](https://apidocs.nextroll.com/user-lists-api/reference.html#get--user-lists-api-v1-userlists-advertisable) |
| [Get User List Sizes by Segment and Date Batch](actions/get-user-list-sizes-by-segment-and-date-batch.md) | `POST /user-lists/api/v1/userlists/segment` | [docs](https://apidocs.nextroll.com/user-lists-api/reference.html#post--user-lists-api-v1-userlists-segment) |
| [Get User List Sizes by Segment and Date with Summary](actions/get-user-list-sizes-by-segment-and-date-with-summary.md) | `GET /user-lists/api/v1/userlists/segment` | [docs](https://apidocs.nextroll.com/user-lists-api/reference.html#get--user-lists-api-v1-userlists-segment) |
| [List Advertisers](actions/list-advertisers.md) | `GET /audience/v1/advertisers` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#get--audience-v1-advertisers) |
| [List Domains in Target Account Lists](actions/list-domains-in-target-account-lists.md) | `GET /audience/v1/target_accounts/domains` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#get--audience-v1-target_accounts-domains) |
| [List ICP Accounts by Advertisable EID](actions/list-icp-accounts-by-advertisable-eid.md) | `POST /audience/v1/ideal_customer_profile/accounts` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#post--audience-v1-ideal_customer_profile-accounts) |
| [List ICPs by Advertisable EID](actions/list-icps-by-advertisable-eid.md) | `GET /audience/v1/ideal_customer_profile` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#get--audience-v1-ideal_customer_profile) |
| [List Scores by TAL EID and Advertisable EID](actions/list-scores-by-tal-eid-and-advertisable-eid.md) | `GET /audience/v1/ideal_customer_profile/all_scores` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#get--audience-v1-ideal_customer_profile-all_scores) |
| [List Segments](actions/list-segments.md) | `GET /audience/v1/segments` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#get--audience-v1-segments) |
| [List Segments with General Exclusions](actions/list-segments-with-general-exclusions.md) | `GET /audience/v1/segments/general_exclusions` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#get--audience-v1-segments-general_exclusions) |
| [List Sharing Invitations](actions/list-sharing-invitations.md) | `GET /audience/v1/sharing/invitation` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#get--audience-v1-sharing-invitation) |
| [List Target Accounts Items](actions/list-target-accounts-items.md) | `GET /audience/v1/target_accounts/:tal_eid/tiers/:ta_tier_eid/items` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#get--audience-v1-target_accounts-(tal_eid)-tiers-(ta_tier_eid)-items) |
| [List Target Accounts List Names and EIDs](actions/list-target-accounts-list-names-and-eids.md) | `GET /audience/v1/target_accounts/names` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#get--audience-v1-target_accounts-names) |
| [List Target Accounts Lists](actions/list-target-accounts-lists.md) | `GET /audience/v1/target_accounts` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#get--audience-v1-target_accounts) |
| [List Target Accounts Lists with General Exclusions](actions/list-target-accounts-lists-with-general-exclusions.md) | `GET /audience/v1/target_accounts/general_exclusions` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#get--audience-v1-target_accounts-general_exclusions) |
| [List Target Accounts Tiers](actions/list-target-accounts-tiers.md) | `GET /audience/v1/target_accounts/:tal_eid/tiers` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#get--audience-v1-target_accounts-(tal_eid)-tiers) |
| [List User Attribute Segments by TAL Reference](actions/list-user-attribute-segments-by-tal-reference.md) | `GET /audience/v1/segments/tal_references` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#get--audience-v1-segments-tal_references) |
| [List User Attributes by Advertisable](actions/list-user-attributes-by-advertisable.md) | `GET /audience/v1/user_attribute_names/:advertisable_eid` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#get--audience-v1-user_attribute_names-(advertisable_eid)) |
| [List Valid and Invalid Segments for Crosschannel LAL Targeting](actions/list-valid-and-invalid-segments-for-crosschannel-lal-targeting.md) | `GET /audience/v1/crosschannel_lal_segments/valid-segments` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#get--audience-v1-crosschannel_lal_segments-valid-segments) |
| [Reactivate Segment](actions/reactivate-segment.md) | `POST /audience/v1/segments/:segment_id/reactivate` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#post--audience-v1-segments-(segment_id)-reactivate) |
| [Revoke Sharing Invitation](actions/revoke-sharing-invitation.md) | `DELETE /audience/v1/sharing/invitation` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#delete--audience-v1-sharing-invitation) |
| [Search Target Accounts Items](actions/search-target-accounts-items.md) | `POST /audience/v1/target_accounts/:tal_eid/tiers/:ta_tier_eid/items/filter` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#post--audience-v1-target_accounts-(tal_eid)-tiers-(ta_tier_eid)-items-filter) |
| [Update ICP by ICP EID and Advertisable EID](actions/update-icp-by-icp-eid-and-advertisable-eid.md) | `POST /audience/v1/ideal_customer_profile/:icp_eid` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#post--audience-v1-ideal_customer_profile-(icp_eid)) |
| [Update Or Delete TAG TAL References](actions/update-or-delete-tag-tal-references.md) | `PUT /audience/v1/segments/tal_references` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#put--audience-v1-segments-tal_references) |
| [Update Segment or Replace User List](actions/update-segment-or-replace-user-list.md) | `POST /audience/v1/segments/:segment_id` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#post--audience-v1-segments-(segment_id)) |
| [Update Target Accounts List](actions/update-target-accounts-list.md) | `POST /audience/v1/target_accounts/:tal_eid` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#post--audience-v1-target_accounts-(tal_eid)) |
| [Update Target Accounts List Items](actions/update-target-accounts-list-items.md) | `PUT /audience/v1/target_accounts/:tal_eid/tiers/:ta_tier_eid/items` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#put--audience-v1-target_accounts-(tal_eid)-tiers-(ta_tier_eid)-items) |
| [Update Target Accounts Tier](actions/update-target-accounts-tier.md) | `POST /audience/v1/target_accounts/:tal_eid/tiers/:ta_tier_eid` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#post--audience-v1-target_accounts-(tal_eid)-tiers-(ta_tier_eid)) |
| [Upsert Target Accounts List Items](actions/upsert-target-accounts-list-items.md) | `POST /audience/v1/target_accounts/:tal_eid/tiers/:ta_tier_eid/items` | [docs](https://apidocs.nextroll.com/audience-api/reference.html#post--audience-v1-target_accounts-(tal_eid)-tiers-(ta_tier_eid)-items) |
