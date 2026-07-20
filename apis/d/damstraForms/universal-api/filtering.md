# Damstra Forms Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Damstra Forms expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Damstra Forms actions that support filtering

- [Get Approver Type](actions/get-approver-type.md)
- [Get Form Integration Representation](actions/get-form-integration-representation.md)
- [Get Project](actions/get-project.md)
- [Get Project List Type](actions/get-project-list-type.md)
- [Get Template](actions/get-template.md)
- [Get User](actions/get-user.md)
- [List Actions](actions/list-actions.md)
- [List Approver Types](actions/list-approver-types.md)
- [List Drawing Annotations](actions/list-drawing-annotations.md)
- [List Drawing Views](actions/list-drawing-views.md)
- [List Drawings](actions/list-drawings.md)
- [List Forms](actions/list-forms.md)
- [List Memos](actions/list-memos.md)
- [List Project List Types](actions/list-project-list-types.md)
- [List Projects](actions/list-projects.md)
- [List Punch Lists](actions/list-punch-lists.md)
- [List Templates](actions/list-templates.md)
- [List Users](actions/list-users.md)
