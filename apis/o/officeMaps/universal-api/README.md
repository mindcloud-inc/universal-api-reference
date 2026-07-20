# <img src="https://images.mindcloud.co/apps/icons/office-maps_1775761317655.png" alt="OfficeMaps logo" width="28" height="28"> OfficeMaps: Universal API

OfficeMaps is workspace management software for interactive office maps, visual staff directories, hot desk booking, car space booking, and meeting room booking.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/officeMaps/latest
- **Category:** Human Resources / HRIS
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://officemaps.io
- **Vendor API docs:** https://api.officemaps.io/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Departments](actions/get-departments.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/get-departments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Department

| Action | Method | Description |
| --- | --- | --- |
| [Add Department Administrator](actions/add-department-administrator.md) | PUT | Adds an administrator to a department in OfficeMaps. |
| [Add Department Manager](actions/add-department-manager.md) | PUT | Adds a manager to a department in OfficeMaps. |
| [Add Department Member](actions/add-department-member.md) | PUT | Adds a member to a department in OfficeMaps. |
| [Bulk Add Department Administrators](actions/bulk-add-department-administrators.md) | PUT | Adds multiple administrators to a department in OfficeMaps. |
| [Bulk Add Department Managers](actions/bulk-add-department-managers.md) | PUT | Adds multiple managers to a department in OfficeMaps. |
| [Bulk Add Department Members](actions/bulk-add-department-members.md) | PUT | Adds multiple members to a department in OfficeMaps. |
| [Bulk Remove Department Administrators](actions/bulk-remove-department-administrators.md) | PUT | Removes multiple administrators from a department in OfficeMaps. |
| [Bulk Remove Department Managers](actions/bulk-remove-department-managers.md) | PUT | Removes multiple managers from a department in OfficeMaps. |
| [Bulk Remove Department Members](actions/bulk-remove-department-members.md) | PUT | Removes multiple members from a department in OfficeMaps. |
| [Get Department Details](actions/get-department-details.md) | GET | Retrieves department details from OfficeMaps. |
| [Get Department Tree List](actions/get-department-tree-list.md) | GET | Retrieves the full department tree from OfficeMaps. |
| [Get Department Tree List By Id](actions/get-department-tree-list-by-id.md) | GET | Retrieves a department tree from OfficeMaps by department ID. |
| [Get Departments](actions/get-departments.md) | GET | Retrieves departments from OfficeMaps with membership data. |
| [Remove Department Administrator](actions/remove-department-administrator.md) | PUT | Removes an administrator from a department in OfficeMaps. |
| [Remove Department Manager](actions/remove-department-manager.md) | PUT | Removes a manager from a department in OfficeMaps. |
| [Remove Department Member](actions/remove-department-member.md) | PUT | Removes a member from a department in OfficeMaps. |

### Employee

| Action | Method | Description |
| --- | --- | --- |
| [Create Person](actions/create-person.md) | POST | Creates a new person in OfficeMaps. |
| [Delete Person](actions/delete-person.md) | DELETE | Deletes an existing person from OfficeMaps. |
| [Get Department Administrators](actions/get-department-administrators.md) | GET | Retrieves administrators in an OfficeMaps department. |
| [Get Department Managers](actions/get-department-managers.md) | GET | Retrieves managers in an OfficeMaps department. |
| [Get Department Members](actions/get-department-members.md) | GET | Retrieves members in an OfficeMaps department. |
| [Get Person](actions/get-person.md) | GET | Retrieves a person from OfficeMaps by ID. |
| [Search Persons](actions/search-persons.md) | GET | Finds people in OfficeMaps by search filters. |
| [Update Person](actions/update-person.md) | PUT | Updates an existing person in OfficeMaps. |

