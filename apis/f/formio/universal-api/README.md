# <img src="https://images.mindcloud.co/apps/icons/formio-square-icon_1775747009489.png" alt="Form.io logo" width="28" height="28"> Form.io: Universal API

Admin API wrapper for Form.io projects, forms, roles, and submissions using a project API key sent on the x-token header.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/formio/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 39
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://form.io
- **Vendor API docs:** https://help.form.io/developers/introduction/api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Project](actions/get-project.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formio/latest/actions/get-project?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (39)

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | POST | Creates a new form in your Form.io project. |
| [Delete Form](actions/delete-form.md) | DELETE | Deletes an existing form from your Form.io project. |
| [Get Form](actions/get-form.md) | GET | Retrieves a form from your Form.io project. |
| [List Forms](actions/list-forms-all.md) | GET | Retrieves forms from your Form.io project. |
| [Search Forms](actions/search-forms.md) | GET | Finds forms in Form.io by title pattern. |
| [Update Form](actions/update-form.md) | PUT | Updates an existing form in your Form.io project. |

### Form Action

| Action | Method | Description |
| --- | --- | --- |
| [Create Form Action](actions/create-form-action.md) | POST | Creates a new form action in your Form.io project. |
| [Delete Form Action](actions/delete-form-action.md) | DELETE | Deletes an existing form action from your Form.io project. |
| [Get Form Action](actions/get-form-action.md) | GET | Retrieves a form action from your Form.io project. |
| [List Form Actions](actions/list-form-actions.md) | GET | Retrieves actions for a form in Form.io. |
| [Update Form Action](actions/update-form-action.md) | PUT | Updates an existing form action in your Form.io project. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Create Admin Submission](actions/create-admin-submission.md) | POST | Creates a new admin submission in your Form.io project. |
| [Create Form Submission](actions/create-form-submission.md) | POST | Creates a new form submission in your Form.io project. |
| [Create User Submission](actions/create-user-submission.md) | POST | Creates a new user submission in your Form.io project. |
| [Delete Admin Submission](actions/delete-admin-submission.md) | DELETE | Deletes an existing admin submission from your Form.io project. |
| [Delete Form Submission](actions/delete-form-submission.md) | DELETE | Deletes an existing form submission from your Form.io project. |
| [Delete User Submission](actions/delete-user-submission.md) | DELETE | Deletes an existing user submission from your Form.io project. |
| [Get Admin Submission](actions/get-admin-submission.md) | GET | Retrieves an admin submission from your Form.io project. |
| [Get Form Submission](actions/get-form-submission.md) | GET | Retrieves a form submission from your Form.io project. |
| [Get User Submission](actions/get-user-submission.md) | GET | Retrieves a user submission from your Form.io project. |
| [List Admin Submissions](actions/list-admin-submissions.md) | GET | Retrieves admin submissions from your Form.io project. |
| [List Form Submissions](actions/list-form-submissions.md) | GET | Retrieves submissions for a form in Form.io. |
| [List User Submissions](actions/list-user-submissions.md) | GET | Retrieves user submissions from your Form.io project. |
| [Update Admin Submission](actions/update-admin-submission.md) | PUT | Updates an existing admin submission in your Form.io project. |
| [Update Form Submission](actions/update-form-submission.md) | PUT | Updates an existing form submission in your Form.io project. |
| [Update User Submission](actions/update-user-submission.md) | PUT | Updates an existing user submission in your Form.io project. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves details for your Form.io project. |

### Project Access

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Access](actions/get-project-access.md) | GET | Retrieves project access details from Form.io. |

### Project Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Token](actions/get-project-token.md) | GET | Retrieves the token for your Form.io project. |

### Resource Form

| Action | Method | Description |
| --- | --- | --- |
| [List Resource Forms](actions/list-resource-forms.md) | GET | Retrieves resource forms from your Form.io project. |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [Create Role](actions/create-role.md) | POST | Creates a new role in your Form.io project. |
| [Get Role](actions/get-role.md) | GET | Retrieves a role from your Form.io project. |
| [List Roles](actions/list-roles.md) | GET | Retrieves roles from your Form.io project. |
| [Search Roles](actions/search-roles.md) | GET | Finds roles in Form.io by title pattern. |
| [Update Role](actions/update-role.md) | PUT | Updates an existing role in your Form.io project. |

### Standard Form

| Action | Method | Description |
| --- | --- | --- |
| [List Standard Forms](actions/list-standard-forms.md) | GET | Retrieves standard forms from your Form.io project. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in your Form.io project. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from your Form.io project. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from your Form.io project. |

