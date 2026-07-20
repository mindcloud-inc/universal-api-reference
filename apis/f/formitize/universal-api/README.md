# <img src="https://images.mindcloud.co/apps/icons/images-16_1775852798963.png" alt="Formitize logo" width="28" height="28"> Formitize: Universal API

Connect to Formitize to work with tasks, forms, clients, contacts, and jobs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/formitize/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://formitize.com
- **Vendor API docs:** https://mitechnologies.github.io/Formitize-NET-API/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tasks](actions/list-tasks.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formitize/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Add Client](actions/add-client.md) | POST | Creates a new client in Formitize. |
| [Delete Client](actions/delete-client.md) | DELETE | Deactivates an existing client in Formitize. |
| [Edit Client](actions/edit-client.md) | PUT | Updates an existing client in Formitize. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from Formitize. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from Formitize. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact](actions/add-contact.md) | POST | Creates a new contact in Formitize. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Formitize. |
| [Edit Contact](actions/edit-contact.md) | PUT | Updates an existing contact in Formitize. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Formitize. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Formitize. |

### Form Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Form Template](actions/get-form-template.md) | GET | Retrieves a form template from Formitize. |
| [List Templates](actions/list-templates.md) | GET | Retrieves form templates from Formitize. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Add Job](actions/add-job.md) | POST | Creates a new job in Formitize. |
| [Delete Job](actions/delete-job.md) | DELETE | Deletes an existing job from Formitize. |
| [Edit Job](actions/edit-job.md) | PUT | Updates an existing job in Formitize. |
| [Get Job](actions/get-job.md) | GET | Retrieves a job from Formitize. |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves jobs from Formitize. |

### Job History

| Action | Method | Description |
| --- | --- | --- |
| [Get Job History](actions/get-job-history.md) | GET | Retrieves a job's history from Formitize. |

### Submitted Form

| Action | Method | Description |
| --- | --- | --- |
| [Get Submitted Form](actions/get-submitted-form.md) | GET | Retrieves a submitted form from Formitize. |
| [List Submitted Forms](actions/list-submitted-forms.md) | GET | Retrieves submitted forms from Formitize. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Formitize. |
| [Delete Task](actions/delete-task.md) | DELETE | Soft deletes an existing task in Formitize. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Formitize. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Formitize. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Formitize. |

