# Qase: Native API Reference

A consolidated summary of Qase's API configuration and 83 documented operations, with links to official documentation.

- **Official docs:** https://developers.qase.io/reference/get-projects
- **OpenAPI specification:** https://developers.qase.io/reference/get-projects
- **API base URL:** `https://api.qase.io/v1`

## Authentication

### API Token

Authenticate Qase requests with the provider-required Token header.

### Credentials

- **API Token:** `apiKey` · required · Qase API token. MindCloud injects this into the shared Token header for every request.

Send these headers with each API request:

```http
Token: <apiKey>
```

[Official authentication documentation](https://developers.qase.io/reference/get-projects)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `result.entities`. The total page count is read from `result.total`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (83 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create test cases in bulk](actions/bulk.md) | `POST /case/:code/bulk` | [docs](https://developers.qase.io/reference/get-projects) |
| [Attach the external issues to the test cases](actions/case-attach-external-issue.md) | `POST /case/:code/external-issue/attach` | [docs](https://developers.qase.io/reference/get-projects) |
| [Detach the external issues from the test cases](actions/case-detach-external-issue.md) | `POST /case/:code/external-issue/detach` | [docs](https://developers.qase.io/reference/get-projects) |
| [Complete a specific run](actions/complete-run.md) | `POST /run/:code/:id/complete` | [docs](https://developers.qase.io/reference/get-projects) |
| [Create a new test case](actions/create-case.md) | `POST /case/:code` | [docs](https://developers.qase.io/reference/get-projects) |
| [Create a new configuration in a particular group](actions/create-configuration.md) | `POST /configuration/:code` | [docs](https://developers.qase.io/reference/get-projects) |
| [Create a new configuration group](actions/create-configuration-group.md) | `POST /configuration/:code/group` | [docs](https://developers.qase.io/reference/get-projects) |
| [Create new Custom Field](actions/create-custom-field.md) | `POST /custom_field` | [docs](https://developers.qase.io/reference/get-projects) |
| [Create a new defect](actions/create-defect.md) | `POST /defect/:code` | [docs](https://developers.qase.io/reference/get-projects) |
| [Create a new environment](actions/create-environment.md) | `POST /environment/:code` | [docs](https://developers.qase.io/reference/get-projects) |
| [Create a new milestone](actions/create-milestone.md) | `POST /milestone/:code` | [docs](https://developers.qase.io/reference/get-projects) |
| [Create a new plan](actions/create-plan.md) | `POST /plan/:code` | [docs](https://developers.qase.io/reference/get-projects) |
| [Create new project](actions/create-project.md) | `POST /project` | [docs](https://developers.qase.io/reference/get-projects) |
| [Create test run result](actions/create-result.md) | `POST /result/:code/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Bulk create test run result](actions/create-result-bulk.md) | `POST /result/:code/:id/bulk` | [docs](https://developers.qase.io/reference/get-projects) |
| [Create a new run](actions/create-run.md) | `POST /run/:code` | [docs](https://developers.qase.io/reference/get-projects) |
| [Create a new shared parameter](actions/create-shared-parameter.md) | `POST /shared_parameter` | [docs](https://developers.qase.io/reference/get-projects) |
| [Create a new shared step](actions/create-shared-step.md) | `POST /shared_step/:code` | [docs](https://developers.qase.io/reference/get-projects) |
| [Create a new test suite](actions/create-suite.md) | `POST /suite/:code` | [docs](https://developers.qase.io/reference/get-projects) |
| [Remove attachment by Hash](actions/delete-attachment.md) | `DELETE /attachment/:hash` | [docs](https://developers.qase.io/reference/get-projects) |
| [Delete test case](actions/delete-case.md) | `DELETE /case/:code/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Delete Custom Field](actions/delete-custom-field.md) | `DELETE /custom_field/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Delete defect](actions/delete-defect.md) | `DELETE /defect/:code/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Delete environment](actions/delete-environment.md) | `DELETE /environment/:code/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Delete milestone](actions/delete-milestone.md) | `DELETE /milestone/:code/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Delete plan](actions/delete-plan.md) | `DELETE /plan/:code/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Delete Project by code](actions/delete-project.md) | `DELETE /project/:code` | [docs](https://developers.qase.io/reference/get-projects) |
| [Delete test run result](actions/delete-result.md) | `DELETE /result/:code/:id/:hash` | [docs](https://developers.qase.io/reference/get-projects) |
| [Delete run](actions/delete-run.md) | `DELETE /run/:code/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Delete shared parameter](actions/delete-shared-parameter.md) | `DELETE /shared_parameter/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Delete shared step](actions/delete-shared-step.md) | `DELETE /shared_step/:code/:hash` | [docs](https://developers.qase.io/reference/get-projects) |
| [Delete test suite](actions/delete-suite.md) | `DELETE /suite/:code/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get attachment by Hash](actions/get-attachment.md) | `GET /attachment/:hash` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get all attachments](actions/get-attachments.md) | `GET /attachment` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get a specific author](actions/get-author.md) | `GET /author/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get all authors](actions/get-authors.md) | `GET /author` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get a specific test case](actions/get-case.md) | `GET /case/:code/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get all test cases](actions/get-cases.md) | `GET /case/:code` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get all configuration groups with configurations](actions/get-configurations.md) | `GET /configuration/:code` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get Custom Field](actions/get-custom-field.md) | `GET /custom_field/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get all Custom Fields](actions/get-custom-fields.md) | `GET /custom_field` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get a specific defect](actions/get-defect.md) | `GET /defect/:code/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get all defects](actions/get-defects.md) | `GET /defect/:code` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get a specific environment](actions/get-environment.md) | `GET /environment/:code/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get all environments](actions/get-environments.md) | `GET /environment/:code` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get a specific milestone](actions/get-milestone.md) | `GET /milestone/:code/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get all milestones](actions/get-milestones.md) | `GET /milestone/:code` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get a specific plan](actions/get-plan.md) | `GET /plan/:code/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get all plans](actions/get-plans.md) | `GET /plan/:code` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get Project by code](actions/get-project.md) | `GET /project/:code` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get test run result by code](actions/get-result.md) | `GET /result/:code/:hash` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get all test run results](actions/get-results.md) | `GET /result/:code` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get a specific run](actions/get-run.md) | `GET /run/:code/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get all runs](actions/get-runs.md) | `GET /run/:code` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get a specific shared parameter](actions/get-shared-parameter.md) | `GET /shared_parameter/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get all shared parameters](actions/get-shared-parameters.md) | `GET /shared_parameter` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get a specific shared step](actions/get-shared-step.md) | `GET /shared_step/:code/:hash` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get all shared steps](actions/get-shared-steps.md) | `GET /shared_step/:code` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get a specific test suite](actions/get-suite.md) | `GET /suite/:code/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get all test suites](actions/get-suites.md) | `GET /suite/:code` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get all System Fields](actions/get-system-fields.md) | `GET /system_field` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get a specific user](actions/get-user.md) | `GET /user/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Get all users](actions/get-users.md) | `GET /user` | [docs](https://developers.qase.io/reference/get-projects) |
| [Grant access to project by code](actions/grant-access-to-project.md) | `POST /project/:code/access` | [docs](https://developers.qase.io/reference/get-projects) |
| [List Projects](actions/list-projects.md) | `GET /project` | [docs](https://developers.qase.io/reference/get-projects) |
| [Resolve a specific defect](actions/resolve-defect.md) | `PATCH /defect/:code/resolve/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Revoke access to project by code](actions/revoke-access-to-project.md) | `DELETE /project/:code/access` | [docs](https://developers.qase.io/reference/get-projects) |
| [Update external issues for runs](actions/run-update-external-issue.md) | `POST /run/:code/external-issue` | [docs](https://developers.qase.io/reference/get-projects) |
| [Search entities by Qase Query Language (QQL)](actions/search.md) | `GET /search` | [docs](https://developers.qase.io/reference/get-projects) |
| [Update test case](actions/update-case.md) | `PATCH /case/:code/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Update Custom Field](actions/update-custom-field.md) | `PATCH /custom_field/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Update defect](actions/update-defect.md) | `PATCH /defect/:code/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Update a specific defect status](actions/update-defect-status.md) | `PATCH /defect/:code/status/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Update environment](actions/update-environment.md) | `PATCH /environment/:code/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Update milestone](actions/update-milestone.md) | `PATCH /milestone/:code/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Update plan](actions/update-plan.md) | `PATCH /plan/:code/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Update test run result](actions/update-result.md) | `PATCH /result/:code/:id/:hash` | [docs](https://developers.qase.io/reference/get-projects) |
| [Update a specific run](actions/update-run.md) | `PATCH /run/:code/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Update publicity of a specific run](actions/update-run-publicity.md) | `PATCH /run/:code/:id/public` | [docs](https://developers.qase.io/reference/get-projects) |
| [Update shared parameter](actions/update-shared-parameter.md) | `PATCH /shared_parameter/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Update shared step](actions/update-shared-step.md) | `PATCH /shared_step/:code/:hash` | [docs](https://developers.qase.io/reference/get-projects) |
| [Update test suite](actions/update-suite.md) | `PATCH /suite/:code/:id` | [docs](https://developers.qase.io/reference/get-projects) |
| [Upload attachment](actions/upload-attachment.md) | `POST /attachment/:code` | [docs](https://developers.qase.io/reference/get-projects) |
