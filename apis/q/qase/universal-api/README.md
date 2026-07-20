# <img src="https://images.mindcloud.co/apps/icons/qase_1776179939021.png" alt="Qase logo" width="28" height="28"> Qase: Universal API

Qase is a test management platform for managing projects, suites, cases, runs, plans, defects, milestones, shared steps, attachments, and related testing resources through the Qase TestOps API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/qase/latest
- **Actions:** 83
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://qase.io
- **Vendor API docs:** https://developers.qase.io/reference/get-projects

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qase/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (83)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Remove attachment by Hash](actions/delete-attachment.md) | DELETE | Deletes an attachment from Qase by hash. |
| [Get attachment by Hash](actions/get-attachment.md) | GET | Retrieves an attachment from Qase by hash. |
| [Get all attachments](actions/get-attachments.md) | GET | Retrieves attachments from Qase. |
| [Upload attachment](actions/upload-attachment.md) | PUT | Uploads an attachment to Qase. |

### Author

| Action | Method | Description |
| --- | --- | --- |
| [Get a specific author](actions/get-author.md) | GET | Retrieves an author from Qase. |
| [Get all authors](actions/get-authors.md) | GET | Retrieves authors from Qase. |

### Case

| Action | Method | Description |
| --- | --- | --- |
| [Create test cases in bulk](actions/bulk.md) | POST | Creates multiple test cases in Qase. |
| [Attach the external issues to the test cases](actions/case-attach-external-issue.md) | PUT | Attaches external issues to test cases in Qase. |
| [Detach the external issues from the test cases](actions/case-detach-external-issue.md) | PUT | Detaches external issues from test cases in Qase. |
| [Create a new test case](actions/create-case.md) | POST | Creates a new test case in Qase. |
| [Delete test case](actions/delete-case.md) | DELETE | Deletes a test case from Qase. |
| [Get a specific test case](actions/get-case.md) | GET | Retrieves a test case from Qase. |
| [Get all test cases](actions/get-cases.md) | GET | Retrieves test cases from Qase. |
| [Update test case](actions/update-case.md) | PUT | Updates an existing test case in Qase. |

### Configuration

| Action | Method | Description |
| --- | --- | --- |
| [Create a new configuration in a particular group](actions/create-configuration.md) | POST | Creates a new configuration in a Qase group. |
| [Create a new configuration group](actions/create-configuration-group.md) | POST | Creates a new configuration group in Qase. |
| [Get all configuration groups with configurations](actions/get-configurations.md) | GET | Retrieves configuration groups and configurations from Qase. |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [Create new Custom Field](actions/create-custom-field.md) | POST | Creates a new custom field in Qase. |
| [Delete Custom Field](actions/delete-custom-field.md) | DELETE | Deletes a custom field from Qase. |
| [Get Custom Field](actions/get-custom-field.md) | GET | Retrieves a custom field from Qase. |
| [Get all Custom Fields](actions/get-custom-fields.md) | GET | Retrieves custom fields from Qase. |
| [Update Custom Field](actions/update-custom-field.md) | PUT | Updates an existing custom field in Qase. |

### Defect

| Action | Method | Description |
| --- | --- | --- |
| [Create a new defect](actions/create-defect.md) | POST | Creates a new defect in Qase. |
| [Delete defect](actions/delete-defect.md) | DELETE | Deletes a defect from Qase. |
| [Get a specific defect](actions/get-defect.md) | GET | Retrieves a defect from Qase. |
| [Get all defects](actions/get-defects.md) | GET | Retrieves defects from Qase. |
| [Resolve a specific defect](actions/resolve-defect.md) | PUT | Resolves a defect in Qase. |
| [Update defect](actions/update-defect.md) | PUT | Updates an existing defect in Qase. |
| [Update a specific defect status](actions/update-defect-status.md) | PUT | Updates a defect status in Qase. |

### Environment

| Action | Method | Description |
| --- | --- | --- |
| [Create a new environment](actions/create-environment.md) | POST | Creates a new environment in Qase. |
| [Delete environment](actions/delete-environment.md) | DELETE | Deletes an environment from Qase. |
| [Get a specific environment](actions/get-environment.md) | GET | Retrieves an environment from Qase. |
| [Get all environments](actions/get-environments.md) | GET | Retrieves environments from Qase. |
| [Update environment](actions/update-environment.md) | PUT | Updates an existing environment in Qase. |

### Milestone

| Action | Method | Description |
| --- | --- | --- |
| [Create a new milestone](actions/create-milestone.md) | POST | Creates a new milestone in Qase. |
| [Delete milestone](actions/delete-milestone.md) | DELETE | Deletes a milestone from Qase. |
| [Get a specific milestone](actions/get-milestone.md) | GET | Retrieves a milestone from Qase. |
| [Get all milestones](actions/get-milestones.md) | GET | Retrieves milestones from Qase. |
| [Update milestone](actions/update-milestone.md) | PUT | Updates an existing milestone in Qase. |

### Plan

| Action | Method | Description |
| --- | --- | --- |
| [Create a new plan](actions/create-plan.md) | POST | Creates a new test plan in Qase. |
| [Delete plan](actions/delete-plan.md) | DELETE | Deletes a test plan from Qase. |
| [Get a specific plan](actions/get-plan.md) | GET | Retrieves a test plan from Qase. |
| [Get all plans](actions/get-plans.md) | GET | Retrieves test plans from Qase. |
| [Update plan](actions/update-plan.md) | PUT | Updates an existing test plan in Qase. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create new project](actions/create-project.md) | POST | Creates a new project in Qase. |
| [Delete Project by code](actions/delete-project.md) | DELETE | Deletes a project from Qase by code. |
| [Get Project by code](actions/get-project.md) | GET | Retrieves a project from Qase by code. |
| [Grant access to project by code](actions/grant-access-to-project.md) | POST | Grants access to a project in Qase. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Qase. |
| [Revoke access to project by code](actions/revoke-access-to-project.md) | DELETE | Revokes access to a project in Qase. |

### Result

| Action | Method | Description |
| --- | --- | --- |
| [Create test run result](actions/create-result.md) | POST | Creates a test run result in Qase. |
| [Bulk create test run result](actions/create-result-bulk.md) | POST | Creates multiple test run results in Qase. |
| [Delete test run result](actions/delete-result.md) | DELETE | Deletes a test run result from Qase. |
| [Get test run result by code](actions/get-result.md) | GET | Retrieves a test run result from Qase by hash. |
| [Get all test run results](actions/get-results.md) | GET | Retrieves test run results from Qase. |
| [Update test run result](actions/update-result.md) | PUT | Updates an existing test run result in Qase. |

### Run

| Action | Method | Description |
| --- | --- | --- |
| [Complete a specific run](actions/complete-run.md) | PUT | Completes a test run in Qase. |
| [Create a new run](actions/create-run.md) | POST | Creates a new test run in Qase. |
| [Delete run](actions/delete-run.md) | DELETE | Deletes a test run from Qase. |
| [Get a specific run](actions/get-run.md) | GET | Retrieves a test run from Qase. |
| [Get all runs](actions/get-runs.md) | GET | Retrieves test runs from Qase. |
| [Update external issues for runs](actions/run-update-external-issue.md) | PUT | Updates external issue links for test runs in Qase. |
| [Update a specific run](actions/update-run.md) | PUT | Updates an existing test run in Qase. |
| [Update publicity of a specific run](actions/update-run-publicity.md) | PUT | Updates test run publicity in Qase. |

### Search

| Action | Method | Description |
| --- | --- | --- |
| [Search entities by Qase Query Language (QQL)](actions/search.md) | GET | Finds entities in Qase using Qase Query Language. |

### Shared Parameter

| Action | Method | Description |
| --- | --- | --- |
| [Create a new shared parameter](actions/create-shared-parameter.md) | POST | Creates a new shared parameter in Qase. |
| [Delete shared parameter](actions/delete-shared-parameter.md) | DELETE | Deletes a shared parameter from Qase. |
| [Get a specific shared parameter](actions/get-shared-parameter.md) | GET | Retrieves a shared parameter from Qase. |
| [Get all shared parameters](actions/get-shared-parameters.md) | GET | Retrieves shared parameters from Qase. |
| [Update shared parameter](actions/update-shared-parameter.md) | PUT | Updates an existing shared parameter in Qase. |

### Shared Step

| Action | Method | Description |
| --- | --- | --- |
| [Create a new shared step](actions/create-shared-step.md) | POST | Creates a new shared step in Qase. |
| [Delete shared step](actions/delete-shared-step.md) | DELETE | Deletes a shared step from Qase. |
| [Get a specific shared step](actions/get-shared-step.md) | GET | Retrieves a shared step from Qase. |
| [Get all shared steps](actions/get-shared-steps.md) | GET | Retrieves shared steps from Qase. |
| [Update shared step](actions/update-shared-step.md) | PUT | Updates an existing shared step in Qase. |

### Suite

| Action | Method | Description |
| --- | --- | --- |
| [Create a new test suite](actions/create-suite.md) | POST | Creates a new test suite in Qase. |
| [Delete test suite](actions/delete-suite.md) | DELETE | Deletes a test suite from Qase. |
| [Get a specific test suite](actions/get-suite.md) | GET | Retrieves a test suite from Qase. |
| [Get all test suites](actions/get-suites.md) | GET | Retrieves test suites from Qase. |
| [Update test suite](actions/update-suite.md) | PUT | Updates an existing test suite in Qase. |

### System Field

| Action | Method | Description |
| --- | --- | --- |
| [Get all System Fields](actions/get-system-fields.md) | GET | Retrieves system fields from Qase. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get a specific user](actions/get-user.md) | GET | Retrieves a user from Qase. |
| [Get all users](actions/get-users.md) | GET | Retrieves users from Qase. |

