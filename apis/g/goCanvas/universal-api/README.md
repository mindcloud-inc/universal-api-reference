# <img src="https://images.mindcloud.co/apps/icons/go-canvas_1789656566689.png" alt="GoCanvas logo" width="28" height="28"> GoCanvas: Universal API

Manage users, department memberships, form assignments, and reference data in GoCanvas.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/goCanvas/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.gocanvas.com
- **Vendor API docs:** https://api.gocanvas.com/api/v3/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Departments

| Action | Method | Description |
| --- | --- | --- |
| [List Departments](actions/list-departments.md) | GET |  |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [List Forms](actions/list-forms.md) | GET |  |

### Reference Data

| Action | Method | Description |
| --- | --- | --- |
| [Create Reference Data](actions/create-reference-data.md) | POST |  |
| [List Reference Data](actions/list-reference-data.md) | GET |  |
| [Retrieve Reference Data](actions/retrieve-reference-data.md) | GET |  |
| [Update Reference Data](actions/update-reference-data.md) | PUT |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Add User to Department](actions/add-user-to-department.md) | POST |  |
| [Assign User to Form](actions/assign-user-to-form.md) | POST |  |
| [Change User Password](actions/change-user-password.md) | PUT |  |
| [Create User](actions/create-user.md) | POST |  |
| [Get Current User](actions/get-current-user.md) | GET |  |
| [List Department Users](actions/list-department-users.md) | GET |  |
| [List Form Users](actions/list-form-users.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |
| [Retrieve User](actions/retrieve-user.md) | GET |  |
| [Unassign User from Form](actions/unassign-user-from-form.md) | DELETE |  |
| [Update User](actions/update-user.md) | PUT |  |

