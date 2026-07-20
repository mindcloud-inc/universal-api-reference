# <img src="https://images.mindcloud.co/apps/icons/plato-forms_1775237021350.png" alt="PlatoForms logo" width="28" height="28"> PlatoForms: Universal API

Convert PDFs and build forms, submissions, and workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/platoForms/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.platoforms.com/
- **Vendor API docs:** https://apidocs.platoforms.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Forms](actions/list-forms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | POST | Creates a new form in PlatoForms. |
| [Create Form Invitation](actions/create-form-invitation.md) | POST | Creates a new form invitation in PlatoForms. |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in PlatoForms. |
| [Delete Form Invitation](actions/delete-form-invitation.md) | DELETE | Deletes an existing form invitation from PlatoForms. |
| [Delete Submission](actions/delete-submission.md) | DELETE | Deletes an existing submission from PlatoForms. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from PlatoForms. |
| [Get Draft Submission Detail](actions/get-draft-submission-detail.md) | GET | Retrieves draft submission details from PlatoForms. |
| [Get Form Fields Definition](actions/get-form-fields-definition.md) | GET | Retrieves form field definitions from PlatoForms. |
| [Get Form Invitation](actions/get-form-invitation.md) | GET | Retrieves form invitation details from PlatoForms. |
| [Get Form Metadata](actions/get-form-metadata.md) | GET | Retrieves metadata for a form from PlatoForms. |
| [Get Submission Detail](actions/get-submission-detail.md) | GET | Retrieves detailed submission data from PlatoForms. |
| [Get Submission Revision History](actions/get-submission-revision-history.md) | GET | Retrieves submission revision history from PlatoForms. |
| [Get Webhook Details](actions/get-webhook-details.md) | GET | Retrieves webhook subscription details from PlatoForms. |
| [Get Webhook Test Data](actions/get-webhook-test-data.md) | GET | Retrieves webhook test data for a form from PlatoForms. |
| [List Form Draft Submissions](actions/list-form-draft-submissions.md) | GET | Retrieves draft form submissions from PlatoForms. |
| [List Form Submissions](actions/list-form-submissions.md) | GET | Retrieves form submission metadata from PlatoForms. |
| [List Form Webhooks](actions/list-form-webhooks.md) | GET | Retrieves webhooks for a form from PlatoForms. |
| [List Forms](actions/list-forms.md) | GET | Retrieves a list of forms from PlatoForms. |
| [Submit Form](actions/submit-form.md) | POST | Creates a new form submission in PlatoForms. |
| [Update Dropdown List Options](actions/update-dropdown-list-options.md) | PUT | Updates dropdown list options for a form in PlatoForms. |
| [Update Form](actions/update-form.md) | PUT | Updates an existing form in PlatoForms. |
| [Update Form Fields](actions/update-form-fields.md) | PUT | Updates form field definitions in PlatoForms. |
| [Update Form Invitation](actions/update-form-invitation.md) | PUT | Updates an existing form invitation in PlatoForms. |
| [Update Form Submission](actions/update-form-submission.md) | PUT | Updates an existing form submission in PlatoForms. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Get Complete Workflow Chain](actions/get-complete-workflow-chain.md) | GET | Retrieves a complete workflow chain from PlatoForms. |
| [List Team Workflows](actions/list-team-workflows.md) | GET | Retrieves team workflow details from PlatoForms. |
| [List Workflow Execution Trees](actions/list-workflow-execution-trees.md) | GET | Retrieves workflow execution trees from PlatoForms. |
| [List Workflow First-Step Submissions](actions/list-workflow-first-step-submissions.md) | GET | Retrieves first-step workflow submissions from PlatoForms. |
| [Submit Workflow Step](actions/submit-workflow-step.md) | POST | Creates a workflow step submission in PlatoForms. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get API User Information](actions/get-api-user-information.md) | GET | Retrieves the current API user's details from PlatoForms. |

