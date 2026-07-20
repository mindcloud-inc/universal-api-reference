# <img src="https://images.mindcloud.co/apps/icons/klipfolio_1782741599377.png" alt="Klipfolio logo" width="28" height="28"> Klipfolio: Universal API

Manage Klipfolio users, groups, roles, dashboards, klips, datasources, and tags with your Klipfolio API key.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/klipfolio/latest
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.klipfolio.com
- **Vendor API docs:** https://apidocs.klipfolio.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Profile](actions/get-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/klipfolio/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Dashboard

| Action | Method | Description |
| --- | --- | --- |
| [List Group Default Tabs](actions/list-group-default-tabs.md) | GET | Retrieves default tabs for a Klipfolio group. |
| [List Tabs](actions/list-tabs.md) | GET |  |

### Datasource

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Source](actions/get-data-source.md) | GET | Retrieves a data source from Klipfolio by ID. |
| [List Data Sources](actions/list-data-sources.md) | GET | Retrieves a list of data sources from Klipfolio. |

### Datasource Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Source Data](actions/get-data-source-data.md) | GET | Retrieves data for a Klipfolio data source. |

### Datasource Instance Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Source Instance Data](actions/get-data-source-instance-data.md) | GET | Retrieves data for a Klipfolio data source instance. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Find Group By External ID](actions/find-group-by-external-id.md) | GET | Finds a Klipfolio group by external ID. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from Klipfolio by ID. |
| [List Groups](actions/list-groups.md) | GET | Retrieves a list of groups from Klipfolio. |
| [List User Groups](actions/list-user-groups.md) | GET | Retrieves groups assigned to a Klipfolio user. |

### Klip

| Action | Method | Description |
| --- | --- | --- |
| [Get Klip](actions/get-klip.md) | GET | Retrieves a Klip from Klipfolio by ID. |
| [List Klips](actions/list-klips.md) | GET | Retrieves a list of Klips from Klipfolio. |
| [List Klips By Data Source](actions/list-klips-by-data-source.md) | GET | Retrieves Klips from Klipfolio by data source ID. |

### Permission

| Action | Method | Description |
| --- | --- | --- |
| [List Role Permissions](actions/list-role-permissions.md) | GET | Retrieves permissions for a Klipfolio role. |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile](actions/get-profile.md) | GET | Retrieves the current user profile from Klipfolio. |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [Get Role](actions/get-role.md) | GET | Retrieves a role from Klipfolio by ID. |
| [List Roles](actions/list-roles.md) | GET | Retrieves a list of roles from Klipfolio. |
| [List User Roles](actions/list-user-roles.md) | GET | Retrieves roles assigned to a Klipfolio user. |

### Share Rights

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Source Share Rights](actions/get-data-source-share-rights.md) | GET | Retrieves share rights for a Klipfolio data source. |
| [Get Klip Share Rights](actions/get-klip-share-rights.md) | GET | Retrieves share rights for a Klip in Klipfolio. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Klipfolio by ID. |
| [List Group Users](actions/list-group-users.md) | GET | Retrieves users assigned to a Klipfolio group. |
| [List Role Users](actions/list-role-users.md) | GET | Retrieves users assigned to a Klipfolio role. |
| [List Users](actions/list-users.md) | GET | Retrieves a list of users from Klipfolio. |

