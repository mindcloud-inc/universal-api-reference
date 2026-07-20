# <img src="https://images.mindcloud.co/apps/icons/rulebricks_1775149454011.png" alt="Rulebricks logo" width="28" height="28"> Rulebricks: Universal API

Decision automation platform for visual rules, flows, and embedded API-driven workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rulebricks/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://rulebricks.com/
- **Vendor API docs:** https://rulebricks.com/docs/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Folders](actions/list-folders.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/list-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Context

| Action | Method | Description |
| --- | --- | --- |
| [Create Context](actions/create-context.md) | POST | Creates a new context in Rulebricks. |
| [Delete Context](actions/delete-context.md) | DELETE | Deletes a context from Rulebricks. |
| [Get Context](actions/get-context.md) | GET | Retrieves a context from Rulebricks. |
| [List Contexts](actions/list-contexts.md) | GET | Retrieves contexts from Rulebricks. |
| [Update Context](actions/update-context.md) | PUT | Updates an existing context in Rulebricks. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Folder](actions/create-or-update-folder.md) | POST | Creates or updates a rule folder in Rulebricks. |
| [Delete Folder](actions/delete-folder.md) | DELETE | Deletes a rule folder from Rulebricks. |
| [List Folders](actions/list-folders.md) | GET | Retrieves rule folders from Rulebricks. |

### Rule

| Action | Method | Description |
| --- | --- | --- |
| [Delete Rule](actions/delete-rule.md) | DELETE | Deletes a rule from Rulebricks. |
| [Export Rule](actions/export-rule.md) | GET | Exports a rule from Rulebricks. |
| [Import Rule](actions/import-rule.md) | POST | Creates or updates a rule in Rulebricks. |
| [List Rules](actions/list-rules.md) | GET | Retrieves rules from Rulebricks. |

### Rule Result

| Action | Method | Description |
| --- | --- | --- |
| [Solve Rule](actions/solve-rule.md) | GET | Executes a rule in Rulebricks. |

### Rule Test

| Action | Method | Description |
| --- | --- | --- |
| [Create Rule Test](actions/create-rule-test.md) | POST | Creates a test for a Rulebricks rule. |
| [Delete Rule Test](actions/delete-rule-test.md) | DELETE | Deletes a test from a Rulebricks rule. |
| [List Rule Tests](actions/list-rule-tests.md) | GET | Retrieves tests for a Rulebricks rule. |

### Value

| Action | Method | Description |
| --- | --- | --- |
| [Delete Dynamic Value](actions/delete-dynamic-value.md) | DELETE | Deletes a dynamic value from Rulebricks. |
| [List Dynamic Values](actions/list-dynamic-values.md) | GET | Retrieves dynamic values from Rulebricks. |
| [Update or Add Dynamic Values](actions/update-or-add-dynamic-values.md) | PUT | Updates or adds dynamic values in Rulebricks. |

