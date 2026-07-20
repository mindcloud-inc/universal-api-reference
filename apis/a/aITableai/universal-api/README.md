# <img src="https://images.mindcloud.co/apps/icons/a-itableai_1778076638646.png" alt="AITable.ai logo" width="28" height="28"> AITable.ai: Universal API

AITable.ai is a spreadsheet-database platform for managing spaces, datasheets, records, fields, views, files, teams, and roles through the AITable Fusion API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aITableai/latest
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://aitable.ai
- **Vendor API docs:** https://developers.aitable.ai/api/reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Member](actions/get-member.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/get-member?connectionId=$CONNECTION_ID&spaceId=string&unitId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Datasheet

| Action | Method | Description |
| --- | --- | --- |
| [Create Datasheet](actions/create-datasheet.md) | POST | Creates a new datasheet in AITable.ai. |

### Embedded Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Embedded Link](actions/create-embedded-link.md) | POST | Creates a new embedded link in AITable.ai. |
| [Delete Embedded Link](actions/delete-embedded-link.md) | DELETE | Deletes an existing embedded link from AITable.ai. |
| [List Embedded Links](actions/list-embedded-links.md) | GET | Retrieves embedded links for a node in AITable.ai. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Field](actions/create-field.md) | POST | Creates a new datasheet field in AITable.ai. |
| [Delete Field](actions/delete-field.md) | DELETE | Deletes an existing datasheet field from AITable.ai. |
| [List Fields](actions/list-fields.md) | GET | Retrieves fields from a datasheet in AITable.ai. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Get Member](actions/get-member.md) | GET | Retrieves a member from a space in AITable.ai. |
| [List Team Members](actions/list-team-members.md) | GET | Retrieves members of a team in AITable.ai. |

### Node

| Action | Method | Description |
| --- | --- | --- |
| [Get Node](actions/get-node.md) | GET | Retrieves a node from a space in AITable.ai. |
| [List Nodes](actions/list-nodes.md) | GET | Retrieves nodes from a space in AITable.ai. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Records](actions/create-records.md) | POST | Creates new records in a datasheet in AITable.ai. |
| [Delete Records](actions/delete-records.md) | DELETE | Deletes existing records from a datasheet in AITable.ai. |
| [List Records](actions/list-records.md) | GET | Retrieves records from a datasheet in AITable.ai. |
| [Update Records](actions/update-records.md) | PUT | Updates existing records in a datasheet in AITable.ai. |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [List Roles](actions/list-roles.md) | GET | Retrieves roles from a space in AITable.ai. |

### Role Unit

| Action | Method | Description |
| --- | --- | --- |
| [List Role Units](actions/list-role-units.md) | GET | Retrieves units under a role in AITable.ai. |

### Space

| Action | Method | Description |
| --- | --- | --- |
| [List Spaces](actions/list-spaces.md) | GET | Retrieves a list of spaces from AITable.ai. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Create Team](actions/create-team.md) | POST | Creates a new team in AITable.ai. |
| [List Sub Teams](actions/list-sub-teams.md) | GET | Retrieves sub teams from AITable.ai. |
| [Update Team](actions/update-team.md) | PUT | Updates an existing team in AITable.ai. |

### View

| Action | Method | Description |
| --- | --- | --- |
| [List Views](actions/list-views.md) | GET | Retrieves views from a datasheet in AITable.ai. |

