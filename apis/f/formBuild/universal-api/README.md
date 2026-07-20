# <img src="https://images.mindcloud.co/apps/icons/form-build_1773349029429.png" alt="123FormBuild logo" width="28" height="28"> 123FormBuild: Universal API

Build forms, collect data, and automate workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/formBuild/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.123formbuilder.com/
- **Vendor API docs:** https://www.123formbuilder.com/developer/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Forms](actions/list-forms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formBuild/latest/actions/list-forms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [List Form Fields](actions/list-form-fields.md) | GET | Retrieves form fields from a form in 123FormBuilder. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | POST | Creates a new form in 123FormBuilder. |
| [Delete Form](actions/delete-form.md) | DELETE | Deletes an existing form from 123FormBuilder. |
| [Delete Multiple Forms](actions/delete-multiple-forms.md) | DELETE | Deletes multiple forms from your 123FormBuilder account. |
| [Get Form](actions/get-form.md) | GET | Retrieves a form from 123FormBuilder. |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms from your 123FormBuilder account. |
| [Update Form](actions/update-form.md) | PUT | Updates an existing form in 123FormBuilder. |

### Form Submissions

| Action | Method | Description |
| --- | --- | --- |
| [Delete Submission](actions/delete-submission.md) | DELETE | Deletes an existing submission from a 123FormBuilder form. |
| [Get Submission](actions/get-submission.md) | GET | Retrieves a submission from a form in 123FormBuilder. |
| [List Submissions](actions/list-submissions.md) | GET | Retrieves submissions from a form in 123FormBuilder. |
| [Update Submission](actions/update-submission.md) | PUT | Updates an existing submission in a 123FormBuilder form. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [List Group Forms](actions/list-group-forms.md) | GET | Retrieves forms from a group in 123FormBuilder. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in 123FormBuilder. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from 123FormBuilder. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from your 123FormBuilder account. |
| [Share Group](actions/share-group.md) | PUT | Shares a group in 123FormBuilder with a user. |
| [Unshare Group](actions/unshare-group.md) | PUT | Removes a user's access to a group in 123FormBuilder. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in 123FormBuilder. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST | Creates a new account in 123FormBuilder when available for your account. |
| [Create Subuser](actions/create-subuser.md) | POST | Creates a new subuser in 123FormBuilder. |
| [List Users](actions/list-users.md) | GET | Retrieves the master user and subusers from 123FormBuilder. |
| [Update Account](actions/update-account.md) | PUT | Updates an existing account in 123FormBuilder. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in 123FormBuilder. |

