# PlatoForms: Native API Reference

A consolidated summary of PlatoForms's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.platoforms.com/
- **OpenAPI specification:** https://apidocs.platoforms.com/swagger.json
- **API base URL:** `https://api.platoforms.com/v4`

## Authentication

### API Key

Use your PlatoForms non-expiry API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://design.platoforms.com/accounts/api/view)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | `POST /form/{{form_identifier}}/` | [docs](https://apidocs.platoforms.com/#operation/form_create) |
| [Create Form Invitation](actions/create-form-invitation.md) | `POST /invitation/prefill/form/{{form_identifier}}/` | [docs](https://apidocs.platoforms.com/#operation/invitation_prefill_form_create) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks/form/{{form_identifier}}/` | [docs](https://apidocs.platoforms.com/#operation/webhooks_form_create) |
| [Delete Form Invitation](actions/delete-form-invitation.md) | `DELETE /invitation/prefill/form/{{form_identifier}}/{{invitation_identifier}}/` | [docs](https://apidocs.platoforms.com/#operation/invitation_prefill_form_delete) |
| [Delete Submission](actions/delete-submission.md) | `DELETE /submission/{{submission_identifier}}/` | [docs](https://apidocs.platoforms.com/#operation/submission_delete) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/{{web_hooks_id}}/` | [docs](https://apidocs.platoforms.com/#operation/webhooks_delete) |
| [Get API User Information](actions/get-api-user-information.md) | `GET /me/` | [docs](https://apidocs.platoforms.com/#operation/me_list) |
| [Get Complete Workflow Chain](actions/get-complete-workflow-chain.md) | `GET /workflow/{{workflow_identifier}}/submission/{{submission_identifier}}/` | [docs](https://apidocs.platoforms.com/#operation/workflow_submission_read) |
| [Get Draft Submission Detail](actions/get-draft-submission-detail.md) | `GET /submission/draft/{{submission_identifier}}/` | [docs](https://apidocs.platoforms.com/#operation/submission_draft_read) |
| [Get Form Fields Definition](actions/get-form-fields-definition.md) | `GET /form/{{form_identifier}}/fields/` | [docs](https://apidocs.platoforms.com/#operation/form_fields_list) |
| [Get Form Invitation](actions/get-form-invitation.md) | `GET /invitation/prefill/form/{{form_identifier}}/{{invitation_identifier}}/` | [docs](https://apidocs.platoforms.com/#operation/invitation_prefill_form_read) |
| [Get Form Metadata](actions/get-form-metadata.md) | `GET /form/{{form_identifier}}/` | [docs](https://apidocs.platoforms.com/#operation/form_read) |
| [Get Submission Detail](actions/get-submission-detail.md) | `GET /submission/{{submission_identifier}}/` | [docs](https://apidocs.platoforms.com/#operation/submission_read) |
| [Get Submission Revision History](actions/get-submission-revision-history.md) | `GET /submission/rev/{{submission_identifier}}/` | [docs](https://apidocs.platoforms.com/#operation/submission_rev_read) |
| [Get Webhook Details](actions/get-webhook-details.md) | `GET /webhooks/{{web_hooks_id}}/` | [docs](https://apidocs.platoforms.com/#operation/webhooks_read) |
| [Get Webhook Test Data](actions/get-webhook-test-data.md) | `GET /form/{{form_identifier}}/webhook/` | [docs](https://apidocs.platoforms.com/#operation/form_webhook_list) |
| [List Form Draft Submissions](actions/list-form-draft-submissions.md) | `GET /form/{{form_identifier}}/submissions/draft/` | [docs](https://apidocs.platoforms.com/#operation/form_submissions_draft_list) |
| [List Form Submissions](actions/list-form-submissions.md) | `GET /form/{{form_identifier}}/submissions/` | [docs](https://apidocs.platoforms.com/#operation/form_submissions_list) |
| [List Form Webhooks](actions/list-form-webhooks.md) | `GET /webhooks/form/{{form_identifier}}/` | [docs](https://apidocs.platoforms.com/#operation/webhooks_form_read) |
| [List Forms](actions/list-forms.md) | `GET /forms/` | [docs](https://apidocs.platoforms.com/#operation/forms_list) |
| [List Team Workflows](actions/list-team-workflows.md) | `GET /workflows/` | [docs](https://apidocs.platoforms.com/#operation/workflows_list) |
| [List Workflow Execution Trees](actions/list-workflow-execution-trees.md) | `GET /workflow/{{workflow_identifier}}/trees/` | [docs](https://apidocs.platoforms.com/#operation/workflow_trees_list) |
| [List Workflow First-Step Submissions](actions/list-workflow-first-step-submissions.md) | `GET /workflow/{{workflow_identifier}}/submissions/ids/` | [docs](https://apidocs.platoforms.com/#operation/workflow_submissions_ids_list) |
| [Submit Form](actions/submit-form.md) | `POST /submit/form/{{form_identifier}}/` | [docs](https://apidocs.platoforms.com/#operation/submit_form_create) |
| [Submit Workflow Step](actions/submit-workflow-step.md) | `POST /workflow/submit/{{workflow_identifier}}/{{previous_submission_identifier}}/` | [docs](https://apidocs.platoforms.com/#operation/workflow_submit_create) |
| [Update Dropdown List Options](actions/update-dropdown-list-options.md) | `POST /form/{{form_identifier}}/field/dropdown/` | [docs](https://apidocs.platoforms.com/#operation/form_field_dropdown_create) |
| [Update Form](actions/update-form.md) | `PATCH /form/{{form_identifier}}/` | [docs](https://apidocs.platoforms.com/#operation/form_partial_update) |
| [Update Form Fields](actions/update-form-fields.md) | `PATCH /form/{{form_identifier}}/fields/` | [docs](https://apidocs.platoforms.com/#operation/form_fields_partial_update) |
| [Update Form Invitation](actions/update-form-invitation.md) | `PUT /invitation/prefill/form/{{form_identifier}}/{{invitation_identifier}}/` | [docs](https://apidocs.platoforms.com/#operation/invitation_prefill_form_update) |
| [Update Form Submission](actions/update-form-submission.md) | `PUT /submit/form/{{form_identifier}}/{{submission_identifier}}/` | [docs](https://apidocs.platoforms.com/#operation/submit_form_update) |
