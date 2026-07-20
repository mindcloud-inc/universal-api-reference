# <img src="https://images.mindcloud.co/apps/icons/memberstack_1773340021081.png" alt="Memberstack logo" width="28" height="28"> Memberstack: Universal API

Manage Memberstack members, plans, and secured content access

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/memberstack/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.memberstack.com
- **Vendor API docs:** https://developers.memberstack.com/admin-rest-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Data Tables](actions/list-data-tables.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/list-data-tables?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Verify Member Token](actions/verify-member-token.md) | GET |  |

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Table](actions/get-data-table.md) | GET |  |
| [List Data Tables](actions/list-data-tables.md) | GET |  |

### Subscribers

| Action | Method | Description |
| --- | --- | --- |
| [Create Member](actions/create-member.md) | POST |  |
| [Delete Member](actions/delete-member.md) | DELETE |  |
| [Get Member](actions/get-member.md) | GET |  |
| [List Members](actions/list-members.md) | GET |  |
| [Update Member](actions/update-member.md) | PUT |  |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Add Free Plan to Member](actions/add-free-plan-to-member.md) | POST |  |
| [Remove Free Plan from Member](actions/remove-free-plan-from-member.md) | DELETE |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Data Record](actions/create-data-record.md) | POST |  |
| [Delete Data Record](actions/delete-data-record.md) | DELETE |  |
| [Query Data Records](actions/query-data-records.md) | GET |  |
| [Update Data Record](actions/update-data-record.md) | PUT |  |

