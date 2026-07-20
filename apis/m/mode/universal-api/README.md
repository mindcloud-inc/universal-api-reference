# <img src="https://images.mindcloud.co/apps/icons/mode-new-2022_1776282111773.png" alt="Mode logo" width="28" height="28"> Mode: Universal API

Mode is an analytics and business intelligence platform for creating reports, managing collections, running analyses, and inspecting workspace activity through a REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mode/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mode.com/
- **Vendor API docs:** https://mode.com/developer/api-reference/introduction/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Collections](actions/list-collections.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mode/latest/actions/list-collections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Audit Logs](actions/retrieve-audit-logs.md) | GET | Retrieve audit log events for a Mode workspace. |

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | POST | Create a collection in a Mode workspace. |
| [Delete Collection](actions/delete-collection.md) | DELETE | Delete a collection from a Mode workspace. |
| [Get Collection](actions/get-collection.md) | GET | Get details for a specific collection in a Mode workspace. |
| [List Collections](actions/list-collections.md) | GET | List collections that are visible in a Mode workspace. |
| [Update Collection](actions/update-collection.md) | PUT | Update a collection in a Mode workspace. |

### Data Sources

| Action | Method | Description |
| --- | --- | --- |
| [List Data Sources](actions/list-data-sources.md) | GET | List data sources connected to a Mode workspace. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Create a group in a Mode workspace. |
| [Delete Group](actions/delete-group.md) | DELETE | Delete a group from a Mode workspace. |
| [Get Group](actions/get-group.md) | GET | Get details for a specific group in a Mode workspace. |
| [List Groups](actions/list-groups.md) | GET | List groups in a Mode workspace. |
| [Update Group](actions/update-group.md) | PUT | Update a group in a Mode workspace. |

### Memberships

| Action | Method | Description |
| --- | --- | --- |
| [Create Collection Membership](actions/create-collection-membership.md) | POST | Add a member to a collection in a Mode workspace. |
| [Create Group Membership](actions/create-group-membership.md) | POST | Add a member to a group in a Mode workspace. |
| [Delete Group Membership](actions/delete-group-membership.md) | DELETE | Remove a member from a group in a Mode workspace. |
| [Get Collection Membership](actions/get-collection-membership.md) | GET | Get details for a specific membership in a Mode collection. |
| [Get Group Membership](actions/get-group-membership.md) | GET | Get details for a specific membership in a Mode group. |
| [List Collection Memberships](actions/list-collection-memberships.md) | GET | List memberships for a specific collection in a Mode workspace. |
| [List Group Memberships](actions/list-group-memberships.md) | GET | List memberships for a specific group in a Mode workspace. |
| [List Workspace Memberships](actions/list-workspace-memberships.md) | GET | List members in a Mode workspace. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [List Reports For Collection](actions/list-reports-for-collection.md) | GET | List reports in a specific Mode collection. |

