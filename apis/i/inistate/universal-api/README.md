# <img src="https://images.mindcloud.co/apps/icons/favicon-1_1774975638270.png" alt="Inistate logo" width="28" height="28"> Inistate: Universal API

Manage Inistate modules, entries, and workflow activities

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/inistate/latest
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://inistate.com/
- **Vendor API docs:** https://app.swaggerhub.com/apis-docs/Inistate/InistateAPI/1.0.0

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Workspace](actions/get-workspace.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inistate/latest/actions/get-workspace?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Stage0 Activity Form

| Action | Method | Description |
| --- | --- | --- |
| [Get Stage0 Create Form](actions/get-stage0-create-form.md) | GET | Retrieves the Stage0 create form from Inistate. |
| [Get Stage0 Edit Form](actions/get-stage0-edit-form.md) | GET | Retrieves the Stage0 edit form from Inistate. |
| [Get Stage0 Quick View Form](actions/get-stage0-quick-view-form.md) | GET | Retrieves the Stage0 quick-view form from Inistate. |
| [Get Stage0 View Form](actions/get-stage0-view-form.md) | GET | Retrieves the Stage0 view form from Inistate. |

### Stage0 Activity Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Stage0 Activity](actions/run-stage0-activity.md) | PUT | Performs a Stage0 activity on an entry in Inistate. |

### Stage0 Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Stage0 Entry](actions/create-stage0-entry.md) | POST | Creates a new Stage0 entry in Inistate. |
| [Delete Stage0 Entry](actions/delete-stage0-entry.md) | DELETE | Deletes an existing Stage0 entry from Inistate. |
| [Duplicate Stage0 Entry](actions/duplicate-stage0-entry.md) | POST | Creates a duplicated Stage0 entry in Inistate. |
| [Update Stage0 Entry](actions/update-stage0-entry.md) | PUT | Updates an existing Stage0 entry in Inistate. |

### Stage0 Entry Page

| Action | Method | Description |
| --- | --- | --- |
| [List Stage0 Entries](actions/list-stage0-entries.md) | GET | Retrieves Stage0 entries from Inistate. |

### Stage0 Listing Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Stage0 Listing Metadata](actions/get-stage0-listing-metadata.md) | GET | Retrieves Stage0 listing metadata from Inistate. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves a workspace from Inistate. |
| [List Workspaces](actions/list-workspaces.md) | GET | Finds workspaces in Inistate by name. |

