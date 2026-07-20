# Tricentis qTest: Native API Reference

A consolidated summary of Tricentis qTest's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.tricentis.com/qtest-saas/content/apis/overview/how_to_use_interactive_api_documentation.htm
- **OpenAPI specification:** https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml
- **API base URL:** `https://mindcloudapps.qtestnet.com/api/v3`

## Authentication

### Bearer token

Use a qTest bearer access token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.tricentis.com/qtest-saas/content/apis/apis/common_apis.htm)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Build](actions/get-build.md) | `GET /projects/{projectId}/builds/{buildId}` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [Get Current Admin Profile](actions/get-current-admin-profile.md) | `GET /admin-profiles/current` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [Get Defect](actions/get-defect.md) | `GET /projects/{projectId}/defects/{defectId}` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [Get Defect Comment](actions/get-defect-comment.md) | `GET /projects/{projectId}/defects/{idOrKey}/comments/{commentId}` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [Get Module](actions/get-module.md) | `GET /projects/{projectId}/modules/{moduleId}` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [Get Object Field](actions/get-object-field.md) | `GET /projects/{projectId}/settings/{objectType}/fields/{fieldId}` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [Get Project](actions/get-project.md) | `GET /projects/{projectId}` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [Get Release](actions/get-release.md) | `GET /projects/{projectId}/releases/{releaseId}` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [Get Requirement](actions/get-requirement.md) | `GET /projects/{projectId}/requirements/{requirementId}` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [Get Requirement Trace Matrix Report](actions/get-requirement-trace-matrix-report.md) | `GET /projects/{projectId}/requirements/trace-matrix-report` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [Get Test Case](actions/get-test-case.md) | `GET /projects/{projectId}/test-cases/{testCaseId}` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [Get Test Run](actions/get-test-run.md) | `GET /projects/{projectId}/test-runs/{testRunId}` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [Get User](actions/get-user.md) | `GET /users/{userId}` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [List Authentication Systems](actions/list-authentication-systems.md) | `GET /auth-systems` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [List Builds](actions/list-builds.md) | `GET /projects/{projectId}/builds` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [List Defect Comments](actions/list-defect-comments.md) | `GET /projects/{projectId}/defects/{idOrKey}/comments` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [List Field Allowed Values](actions/list-field-allowed-values.md) | `GET /projects/{projectId}/settings/{objectType}/fields/{fieldId}/allowed-values` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [List Jira Connections](actions/list-jira-connections.md) | `GET /projects/{projectId}/settings/integration/connections` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [List Linked Artifacts](actions/list-linked-artifacts.md) | `GET /projects/{projectId}/linked-artifacts` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [List Modules](actions/list-modules.md) | `GET /projects/{projectId}/modules` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [List Object Fields](actions/list-object-fields.md) | `GET /projects/{projectId}/settings/{objectType}/fields` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://docs.tricentis.com/qtest-saas/content/apis/apis/common_apis.htm) |
| [List Recently Updated Defects](actions/list-recently-updated-defects.md) | `GET /projects/{projectId}/defects/last-change` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [List Releases](actions/list-releases.md) | `GET /projects/{projectId}/releases` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [List Requirement Defects](actions/list-requirement-defects.md) | `GET /projects/{projectId}/requirements/{requirementId}/defects` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [List Requirement Test Runs](actions/list-requirement-test-runs.md) | `GET /projects/{projectId}/requirements/{requirementId}/test-runs` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [List Requirements](actions/list-requirements.md) | `GET /projects/{projectId}/requirements` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [List Test Case Versions](actions/list-test-case-versions.md) | `GET /projects/{projectId}/test-cases/{testCaseId}/versions` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [List Test Cases](actions/list-test-cases.md) | `GET /projects/{projectId}/test-cases` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [List Test Logs](actions/list-test-logs.md) | `GET /projects/{projectId}/test-runs/{testRunId}/test-logs` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [List Test Run Statuses](actions/list-test-run-statuses.md) | `GET /projects/{projectId}/test-runs/execution-statuses` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [List Test Runs](actions/list-test-runs.md) | `GET /projects/{projectId}/test-runs` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [List Test Steps](actions/list-test-steps.md) | `GET /projects/{projectId}/test-cases/{testCaseId}/test-steps` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [List Test Suites](actions/list-test-suites.md) | `GET /projects/{projectId}/test-suites` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [List User Groups](actions/list-user-groups.md) | `GET /groups` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [Query Comments](actions/query-comments.md) | `POST /projects/{projectId}/comments` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [Query Object Histories](actions/query-object-histories.md) | `POST /projects/{projectId}/histories` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [Search Attachments](actions/search-attachments.md) | `GET /projects/{projectId}/attachments` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [Search Project Objects](actions/search-project-objects.md) | `POST /projects/{projectId}/search` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
| [Search Projects](actions/search-projects.md) | `POST /projects/search` | [docs](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml) |
