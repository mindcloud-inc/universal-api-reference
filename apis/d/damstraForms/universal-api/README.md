# <img src="https://images.mindcloud.co/apps/icons/damstra-forms_1776788361027.png" alt="Damstra Forms logo" width="28" height="28"> Damstra Forms: Universal API

Damstra Forms provides API access to digital form, project, template, user, drawing, punch list, and workflow records for connected Damstra Forms workspaces.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/damstraForms/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://damstratechnology.com/products/digital-forms
- **Vendor API docs:** https://sammapi.docs.apiary.io/#

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Action

| Action | Method | Description |
| --- | --- | --- |
| [Create Draft Action](actions/create-draft-action.md) | POST | Creates a draft action in Damstra Forms. |
| [Get Action](actions/get-action.md) | GET | Retrieves an action from Damstra Forms. |
| [List Actions](actions/list-actions.md) | GET | Retrieves actions from Damstra Forms. |
| [Update Action](actions/update-action.md) | PUT | Updates an action in Damstra Forms. |

### Approver Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Approver Type](actions/get-approver-type.md) | GET | Retrieves an approver type from Damstra Forms. |
| [List Approver Types](actions/list-approver-types.md) | GET | Retrieves approver types from Damstra Forms. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET | Retrieves a company from Damstra Forms. |

### Drawing

| Action | Method | Description |
| --- | --- | --- |
| [Get Drawing](actions/get-drawing.md) | GET | Retrieves a drawing from Damstra Forms. |
| [List Drawings](actions/list-drawings.md) | GET | Retrieves drawings from Damstra Forms. |

### Drawing Annotation

| Action | Method | Description |
| --- | --- | --- |
| [List Drawing Annotations](actions/list-drawing-annotations.md) | GET | Retrieves drawing annotations from Damstra Forms. |

### Drawing View

| Action | Method | Description |
| --- | --- | --- |
| [List Drawing Views](actions/list-drawing-views.md) | GET | Retrieves drawing views from Damstra Forms. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Close Form](actions/close-form.md) | PUT | Closes a form in Damstra Forms. |
| [Create Draft Form](actions/create-draft-form.md) | POST | Creates a draft form in Damstra Forms. |
| [Get Form](actions/get-form.md) | GET | Retrieves a form from Damstra Forms. |
| [Get Form Integration Representation](actions/get-form-integration-representation.md) | GET | Retrieves a form in integration format from Damstra Forms. |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms from Damstra Forms. |
| [Update Form](actions/update-form.md) | PUT | Updates a form in Damstra Forms. |

### Memo

| Action | Method | Description |
| --- | --- | --- |
| [Create Draft Memo](actions/create-draft-memo.md) | POST | Creates a draft memo in Damstra Forms. |
| [Get Memo](actions/get-memo.md) | GET | Retrieves a memo from Damstra Forms. |
| [List Memos](actions/list-memos.md) | GET | Retrieves memos from Damstra Forms. |

### Organisation

| Action | Method | Description |
| --- | --- | --- |
| [Get Organisation](actions/get-organisation.md) | GET | Retrieves the organisation from Damstra Forms. |

### Organisation List

| Action | Method | Description |
| --- | --- | --- |
| [Get Organisation List](actions/get-organisation-list.md) | GET | Retrieves an organisation list from Damstra Forms. |
| [List Organisation Lists](actions/list-organisation-lists.md) | GET | Retrieves organisation lists from Damstra Forms. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Damstra Forms. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Damstra Forms. |

### Project List

| Action | Method | Description |
| --- | --- | --- |
| [Get Project List](actions/get-project-list.md) | GET | Retrieves a project list from Damstra Forms. |
| [List Project Lists](actions/list-project-lists.md) | GET | Retrieves project lists from Damstra Forms. |

### Project List Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Project List Type](actions/get-project-list-type.md) | GET | Retrieves a project list type from Damstra Forms. |
| [List Project List Types](actions/list-project-list-types.md) | GET | Retrieves project list types from Damstra Forms. |

### Project Member

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Member](actions/get-project-member.md) | GET | Retrieves a project member from Damstra Forms. |
| [List Project Members](actions/list-project-members.md) | GET | Retrieves project members from Damstra Forms. |

### Punch List

| Action | Method | Description |
| --- | --- | --- |
| [Get Punch List](actions/get-punch-list.md) | GET | Retrieves a punch list from Damstra Forms. |
| [List Punch Lists](actions/list-punch-lists.md) | GET | Retrieves punch lists from Damstra Forms. |

### Submission

| Action | Method | Description |
| --- | --- | --- |
| [Get Submission Status](actions/get-submission-status.md) | GET | Retrieves the status of a submitted request from Damstra Forms. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from Damstra Forms. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from Damstra Forms. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Damstra Forms. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Damstra Forms. |

### Wbs Item

| Action | Method | Description |
| --- | --- | --- |
| [Get WBS Item](actions/get-wbs-item.md) | GET | Retrieves a WBS item from Damstra Forms. |
| [List WBS Items](actions/list-wbs-items.md) | GET | Retrieves project WBS items from Damstra Forms. |

