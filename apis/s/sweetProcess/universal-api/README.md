# <img src="https://images.mindcloud.co/apps/icons/sweet-process_1774459695960.png" alt="SweetProcess logo" width="28" height="28"> SweetProcess: Universal API

Manage procedures, tasks, teammates, and process documentation

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sweetProcess/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.sweetprocess.com
- **Vendor API docs:** https://www.sweetprocess.com/kb/8LBTequD/article/L4CaqHMav/interim-api-documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Procedures](actions/list-procedures.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sweetProcess/latest/actions/list-procedures?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Invitation

| Action | Method | Description |
| --- | --- | --- |
| [Create Invitation](actions/create-invitation.md) | POST | Creates a new invitation in SweetProcess. |

### Procedure

| Action | Method | Description |
| --- | --- | --- |
| [Get Procedure](actions/get-procedure.md) | GET | Retrieves a procedure from SweetProcess. |
| [List Procedures](actions/list-procedures.md) | GET | Retrieves procedures from SweetProcess. |

### Taskinstance

| Action | Method | Description |
| --- | --- | --- |
| [List Taskinstances](actions/list-taskinstances.md) | GET | Retrieves task instances from SweetProcess. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Create Team](actions/create-team.md) | POST |  |
| [Delete Team](actions/delete-team.md) | DELETE |  |
| [List Teams](actions/list-teams.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new teammate in SweetProcess. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes an existing teammate from SweetProcess. |
| [List Users](actions/list-users.md) | GET | Retrieves users from SweetProcess. |
| [Update User](actions/update-user.md) | PUT | Updates an existing teammate in SweetProcess. |

