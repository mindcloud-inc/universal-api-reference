# <img src="https://images.mindcloud.co/apps/icons/form-robin_1774635898206.png" alt="FormRobin logo" width="28" height="28"> FormRobin: Universal API

Manage forms, folders, and form submissions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/formRobin/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://formrobin.com
- **Vendor API docs:** https://formrobin.com/developer/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formRobin/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Form Submissions

| Action | Method | Description |
| --- | --- | --- |
| [List Form Sessions](actions/list-form-sessions.md) | GET | Retrieves form sessions for a specific form in FormRobin. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | POST | Creates a new form in FormRobin. |
| [Delete Form](actions/delete-form.md) | DELETE | Deletes an existing form from FormRobin. |
| [Get Form](actions/get-form.md) | GET | Retrieves a form from FormRobin. |
| [List Forms](actions/list-forms.md) | GET | Retrieves a list of forms from FormRobin. |
| [Update Form](actions/update-form.md) | PUT | Updates an existing form in FormRobin. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from FormRobin. |

