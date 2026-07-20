# <img src="https://images.mindcloud.co/apps/icons/flokzu_1775220765277.png" alt="Flokzu logo" width="28" height="28"> Flokzu: Universal API

Flokzu API integration for process instances, database records, user management, and commons.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/flokzu/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://flokzu.com/
- **Vendor API docs:** https://flokzu.docs.apiary.io/reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Echo](actions/echo.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flokzu/latest/actions/echo?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Databases

| Action | Method | Description |
| --- | --- | --- |
| [Add Record](actions/add-record.md) | POST |  |
| [Get Record](actions/get-record.md) | GET |  |
| [List Records](actions/list-records.md) | GET |  |
| [Update Record](actions/update-record.md) | PUT |  |

### Invitations

| Action | Method | Description |
| --- | --- | --- |
| [Send New User Invitation](actions/send-new-user-invitation.md) | POST |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Process Instance](actions/create-process-instance.md) | POST |  |
| [Echo](actions/echo.md) | GET |  |
| [Get Process Instance](actions/get-process-instance.md) | GET |  |
| [List Assignees](actions/list-assignees.md) | GET |  |
| [Operations](actions/operations.md) | GET |  |
| [Update Process Instance](actions/update-process-instance.md) | PUT |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Add User Role](actions/add-user-role.md) | PUT |  |
| [Delete User Account](actions/delete-user-account.md) | DELETE |  |
| [List User Roles](actions/list-user-roles.md) | GET |  |
| [Remove User Role](actions/remove-user-role.md) | PUT |  |

