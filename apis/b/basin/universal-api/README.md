# <img src="https://images.mindcloud.co/apps/icons/basin_1773670708999.png" alt="Basin logo" width="28" height="28"> Basin: Universal API

Manage Basin forms, submissions, projects, and webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/basin/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://usebasin.com
- **Vendor API docs:** https://usebasin.com/api_docs/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Domains](actions/list-domains.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/basin/latest/actions/list-domains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [List Domains](actions/list-domains.md) | GET | Retrieves domain records from Basin. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | POST | Creates a new form in Basin. |
| [Delete Form](actions/delete-form.md) | DELETE | Deletes an existing form from Basin. |
| [List Forms](actions/list-forms.md) | GET | Retrieves form records from Basin. |
| [Show Form](actions/show-form.md) | GET | Retrieves form details from Basin. |
| [Update Form](actions/update-form.md) | PUT | Updates an existing form in Basin. |

### Form View

| Action | Method | Description |
| --- | --- | --- |
| [List Form Views](actions/list-form-views.md) | GET | Retrieves form view records from Basin. |
| [Show Form View](actions/show-form-view.md) | GET | Retrieves form view details from Basin. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Basin. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Basin. |
| [List Projects](actions/list-projects.md) | GET | Retrieves project records from Basin. |
| [Show Project](actions/show-project.md) | GET | Retrieves project details from Basin. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Basin. |

### Submission

| Action | Method | Description |
| --- | --- | --- |
| [Delete Submission](actions/delete-submission.md) | DELETE | Deletes an existing submission from Basin. |
| [List Submissions](actions/list-submissions.md) | GET | Retrieves submission records from Basin. |
| [Refire Submission Webhooks](actions/refire-submission-webhooks.md) | POST | Re-fires webhooks for one submission in Basin. |
| [Refire Submission Webhooks Batch](actions/refire-submission-webhooks-batch.md) | POST | Re-fires webhooks for multiple submissions in Basin. |
| [Show Submission](actions/show-submission.md) | GET | Retrieves submission details from Basin. |
| [Update Submission](actions/update-submission.md) | PUT | Updates an existing submission in Basin. |

