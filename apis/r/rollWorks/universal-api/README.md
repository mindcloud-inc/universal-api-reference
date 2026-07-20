# <img src="https://images.mindcloud.co/apps/icons/rollworks-logo_1775169400057.jpeg" alt="RollWorks logo" width="28" height="28"> RollWorks: Universal API

Manage RollWorks audiences, target accounts, segments, and reporting

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rollWorks/latest
- **Category:** Marketing
- **Actions:** 57
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.adroll.com/solutions/account-based-marketing
- **Vendor API docs:** https://apidocs.nextroll.com/guides/get-started-rollworks.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Advertisers](actions/list-advertisers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rollWorks/latest/actions/list-advertisers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (57)

### Advertiser

| Action | Method | Description |
| --- | --- | --- |
| [List Advertisers](actions/list-advertisers.md) | GET | Retrieves advertisers from RollWorks. |

### Audience Preview

| Action | Method | Description |
| --- | --- | --- |
| [Estimate Composite Segment Size](actions/estimate-composite-segment-size.md) | GET | Retrieves a composite segment size estimate from RollWorks. |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [List Domains in Target Account Lists](actions/list-domains-in-target-account-lists.md) | GET | Retrieves domains in RollWorks target account lists. |

### Domain Reference

| Action | Method | Description |
| --- | --- | --- |
| [Get Domain References](actions/get-domain-references.md) | GET | Retrieves domain references from RollWorks target account lists. |

### Exact Metric

| Action | Method | Description |
| --- | --- | --- |
| [Get Exact User Counts by Date and Metric](actions/get-exact-user-counts-by-date-and-metric.md) | GET | Retrieves exact user counts in RollWorks by date and metric. |

### Icp Account

| Action | Method | Description |
| --- | --- | --- |
| [List ICP Accounts by Advertisable EID](actions/list-icp-accounts-by-advertisable-eid.md) | GET | Retrieves ICP accounts in RollWorks by advertisable EID. |

### Icp Score

| Action | Method | Description |
| --- | --- | --- |
| [List Scores by TAL EID and Advertisable EID](actions/list-scores-by-tal-eid-and-advertisable-eid.md) | GET | Retrieves ICP scores in RollWorks by TAL and advertisable EID. |

### Ideal Customer Profile

| Action | Method | Description |
| --- | --- | --- |
| [Create ICP by Advertisable EID](actions/create-icp-by-advertisable-eid.md) | POST | Creates an ideal customer profile in RollWorks by advertisable EID. |
| [Delete ICP by ICP EID and Advertisable EID](actions/delete-icp-by-icp-eid-and-advertisable-eid.md) | DELETE | Deletes an ideal customer profile from RollWorks by ICP and advertisable EID. |
| [Get ICP by ICP EID and Advertisable EID](actions/get-icp-by-icp-eid-and-advertisable-eid.md) | GET | Retrieves an ideal customer profile from RollWorks by ICP and advertisable EID. |
| [List ICPs by Advertisable EID](actions/list-icps-by-advertisable-eid.md) | GET | Retrieves ideal customer profiles in RollWorks by advertisable EID. |
| [Update ICP by ICP EID and Advertisable EID](actions/update-icp-by-icp-eid-and-advertisable-eid.md) | PUT | Updates an ideal customer profile in RollWorks by ICP and advertisable EID. |

### Mirror Segment

| Action | Method | Description |
| --- | --- | --- |
| [Accept Segment Sharing Invitation](actions/accept-segment-sharing-invitation.md) | POST | Accepts a segment sharing invitation in RollWorks. |
| [Delete Mirror Segment](actions/delete-mirror-segment.md) | DELETE | Deletes a mirror segment from RollWorks. |

### Reporting Query

| Action | Method | Description |
| --- | --- | --- |
| [Execute GraphQL queries](actions/execute-graphql-queries.md) | GET | Executes a GraphQL query in RollWorks. |

### Segment

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Create Or Update Segments by Bulk Route](actions/bulk-create-or-update-segments-by-bulk-route.md) | PUT | Creates or updates segments in bulk in RollWorks. |
| [Bulk Create Or Update Segments by Put Route](actions/bulk-create-or-update-segments-by-put-route.md) | PUT | Creates or updates segments in bulk in RollWorks. |
| [Create Segment](actions/create-segment.md) | POST | Creates a new segment in RollWorks. |
| [Delete Segment](actions/delete-segment.md) | DELETE | Deletes a segment from RollWorks. |
| [Get Segment](actions/get-segment.md) | GET | Retrieves a segment from RollWorks. |
| [List Segments](actions/list-segments.md) | GET | Retrieves segments from RollWorks. |
| [List Segments with General Exclusions](actions/list-segments-with-general-exclusions.md) | GET | Retrieves segments with general exclusions from RollWorks. |
| [List User Attribute Segments by TAL Reference](actions/list-user-attribute-segments-by-tal-reference.md) | GET | Retrieves user attribute segments in RollWorks by TAL reference. |
| [List Valid and Invalid Segments for Crosschannel LAL Targeting](actions/list-valid-and-invalid-segments-for-crosschannel-lal-targeting.md) | GET | Retrieves valid and invalid segments for RollWorks crosschannel LAL targeting. |
| [Reactivate Segment](actions/reactivate-segment.md) | PUT | Reactivates a segment in RollWorks. |
| [Update Or Delete TAG TAL References](actions/update-or-delete-tag-tal-references.md) | PUT | Updates or deletes TAG TAL references in RollWorks. |
| [Update Segment or Replace User List](actions/update-segment-or-replace-user-list.md) | PUT | Updates a segment or replaces its user list in RollWorks. |

### Segment Sharing Invitation

| Action | Method | Description |
| --- | --- | --- |
| [Create Segment Sharing Invitation](actions/create-segment-sharing-invitation.md) | POST | Creates a segment sharing invitation in RollWorks. |
| [List Sharing Invitations](actions/list-sharing-invitations.md) | GET | Retrieves sharing invitations from RollWorks. |
| [Revoke Sharing Invitation](actions/revoke-sharing-invitation.md) | DELETE | Revokes a sharing invitation in RollWorks. |

### Source Segment

| Action | Method | Description |
| --- | --- | --- |
| [Get Source Segment for Sharing Invitation](actions/get-source-segment-for-sharing-invitation.md) | GET | Retrieves the source segment for a RollWorks sharing invitation. |

### Target Accounts Item

| Action | Method | Description |
| --- | --- | --- |
| [Delete Target Accounts List Items by Delete Route](actions/delete-target-accounts-list-items-by-delete-route.md) | DELETE | Deletes target account list items from RollWorks. |
| [Delete Target Accounts List Items by Post Delete Route](actions/delete-target-accounts-list-items-by-post-delete-route.md) | DELETE | Deletes target account list items from RollWorks. |
| [List Target Accounts Items](actions/list-target-accounts-items.md) | GET | Retrieves target account items from RollWorks. |
| [Search Target Accounts Items](actions/search-target-accounts-items.md) | GET | Finds target account items in RollWorks. |
| [Update Target Accounts List Items](actions/update-target-accounts-list-items.md) | PUT | Updates target account list items in RollWorks. |
| [Upsert Target Accounts List Items](actions/upsert-target-accounts-list-items.md) | PUT | Upserts target account list items in RollWorks. |

### Target Accounts List

| Action | Method | Description |
| --- | --- | --- |
| [Create Target Accounts List](actions/create-target-accounts-list.md) | POST | Creates a target account list in RollWorks. |
| [Delete Target Accounts List](actions/delete-target-accounts-list.md) | DELETE | Deletes a target account list from RollWorks. |
| [Get Target Accounts List](actions/get-target-accounts-list.md) | GET | Retrieves a target account list from RollWorks. |
| [List Target Accounts List Names and EIDs](actions/list-target-accounts-list-names-and-eids.md) | GET | Retrieves target account list names and EIDs from RollWorks. |
| [List Target Accounts Lists](actions/list-target-accounts-lists.md) | GET | Retrieves target account lists from RollWorks. |
| [List Target Accounts Lists with General Exclusions](actions/list-target-accounts-lists-with-general-exclusions.md) | GET | Retrieves target account lists with general exclusions from RollWorks. |
| [Update Target Accounts List](actions/update-target-accounts-list.md) | PUT | Updates a target account list in RollWorks. |

### Target Accounts Tier

| Action | Method | Description |
| --- | --- | --- |
| [Create Target Accounts Tier](actions/create-target-accounts-tier.md) | POST | Creates a target account tier in RollWorks. |
| [Delete Target Accounts Tier](actions/delete-target-accounts-tier.md) | DELETE | Deletes a target account tier from RollWorks. |
| [Get Target Accounts Tier](actions/get-target-accounts-tier.md) | GET | Retrieves a target account tier from RollWorks. |
| [List Target Accounts Tiers](actions/list-target-accounts-tiers.md) | GET | Retrieves target account tiers from RollWorks. |
| [Update Target Accounts Tier](actions/update-target-accounts-tier.md) | PUT | Updates a target account tier in RollWorks. |

### User Attribute

| Action | Method | Description |
| --- | --- | --- |
| [List User Attributes by Advertisable](actions/list-user-attributes-by-advertisable.md) | GET | Retrieves user attributes from RollWorks by advertisable. |

### User Attribute Count

| Action | Method | Description |
| --- | --- | --- |
| [Get User Attribute Counts by Name and Value](actions/get-user-attribute-counts-by-name-and-value.md) | GET | Retrieves user attribute counts in RollWorks by name and value. |

### User List Metric

| Action | Method | Description |
| --- | --- | --- |
| [Get CDP Plus User List Sizes by Segment and Date](actions/get-cdp-plus-user-list-sizes-by-segment-and-date.md) | GET | Retrieves CDP Plus user list sizes in RollWorks by segment and date. |
| [Get User List Sizes by Ad and Date](actions/get-user-list-sizes-by-ad-and-date.md) | GET | Retrieves user list sizes in RollWorks by ad and date. |
| [Get User List Sizes by Ad Group and Date](actions/get-user-list-sizes-by-ad-group-and-date.md) | GET | Retrieves user list sizes in RollWorks by ad group and date. |
| [Get User List Sizes by Advertisable and Date](actions/get-user-list-sizes-by-advertisable-and-date.md) | GET | Retrieves user list sizes in RollWorks by advertisable and date. |
| [Get User List Sizes by Segment and Date Batch](actions/get-user-list-sizes-by-segment-and-date-batch.md) | GET | Retrieves user list sizes in RollWorks by segment and date batch. |
| [Get User List Sizes by Segment and Date with Summary](actions/get-user-list-sizes-by-segment-and-date-with-summary.md) | GET | Retrieves user list sizes in RollWorks by segment and date. |

