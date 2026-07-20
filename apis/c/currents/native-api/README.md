# Currents: Native API Reference

A consolidated summary of Currents's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.currents.dev/api
- **API base URL:** `https://api.currents.dev/v1`

## Authentication

### API Key

Authenticate with a Currents API key using Authorization: Bearer <api_key>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.currents.dev/api/get-started/authentication)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Test Signature](actions/generate-test-signature.md) | `POST /signature/test` | [docs](https://docs.currents.dev/resources/api/api-resources/test-signature) |
| [Get Action](actions/get-action.md) | `GET /actions/:actionId` | [docs](https://docs.currents.dev/api/resources) |
| [Get Affected Test Executions](actions/get-affected-test-executions.md) | `GET /actions/tests/:signature` | [docs](https://docs.currents.dev/api/resources) |
| [Get Instance](actions/get-instance.md) | `GET /instances/:instanceId` | [docs](https://docs.currents.dev/resources/api/api-resources/instances) |
| [Get Project](actions/get-project.md) | `GET /projects/:projectId` | [docs](https://docs.currents.dev/resources/api/api-resources/projects) |
| [Get Project Insights](actions/get-project-insights.md) | `GET /projects/:projectId/insights` | [docs](https://docs.currents.dev/resources/api/api-resources/projects) |
| [Get Run](actions/get-run.md) | `GET /runs/:runId` | [docs](https://docs.currents.dev/resources/api/api-resources/runs) |
| [Get Test Results](actions/get-test-results.md) | `GET /test-results/:signature` | [docs](https://docs.currents.dev/api/resources) |
| [List Action Executions](actions/list-action-executions.md) | `GET /actions/:actionId/tests` | [docs](https://docs.currents.dev/api/resources) |
| [List Action Tests](actions/list-action-tests.md) | `GET /actions/:actionId/tests` | [docs](https://docs.currents.dev/api/resources) |
| [List Actions](actions/list-actions.md) | `GET /actions` | [docs](https://docs.currents.dev/api/resources) |
| [List Active Actions](actions/list-active-actions.md) | `GET /actions` | [docs](https://docs.currents.dev/api/resources) |
| [List Affected Tests](actions/list-affected-tests.md) | `GET /actions/tests` | [docs](https://docs.currents.dev/api/resources) |
| [List Disabled Actions](actions/list-disabled-actions.md) | `GET /actions` | [docs](https://docs.currents.dev/api/resources) |
| [List Failing Spec Files](actions/list-failing-spec-files.md) | `GET /spec-files/:projectId` | [docs](https://docs.currents.dev/resources/api/api-resources/spec-files) |
| [List Failing Tests](actions/list-failing-tests.md) | `GET /tests/:projectId` | [docs](https://docs.currents.dev/resources/api/api-resources/tests) |
| [List Flaky Tests](actions/list-flaky-tests.md) | `GET /tests/:projectId` | [docs](https://docs.currents.dev/resources/api/api-resources/tests) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://docs.currents.dev/resources/api/api-resources/projects) |
| [List Quarantined Tests](actions/list-quarantined-tests.md) | `GET /actions/tests` | [docs](https://docs.currents.dev/api/resources) |
| [List Runs](actions/list-runs.md) | `GET /projects/:projectId/runs` | [docs](https://docs.currents.dev/resources/api/api-resources/runs) |
| [List Skipped Tests](actions/list-skipped-tests.md) | `GET /actions/tests` | [docs](https://docs.currents.dev/api/resources) |
| [List Slow Spec Files](actions/list-slow-spec-files.md) | `GET /spec-files/:projectId` | [docs](https://docs.currents.dev/resources/api/api-resources/spec-files) |
| [List Slow Tests](actions/list-slow-tests.md) | `GET /tests/:projectId` | [docs](https://docs.currents.dev/resources/api/api-resources/tests) |
| [List Spec Files](actions/list-spec-files.md) | `GET /spec-files/:projectId` | [docs](https://docs.currents.dev/api/resources) |
| [List Tagged Tests](actions/list-tagged-tests.md) | `GET /actions/tests` | [docs](https://docs.currents.dev/api/resources) |
| [List Tests](actions/list-tests.md) | `GET /tests/:projectId` | [docs](https://docs.currents.dev/api/resources) |
| [Search Actions](actions/search-actions.md) | `GET /actions` | [docs](https://docs.currents.dev/api/resources) |
| [Search Affected Tests](actions/search-affected-tests.md) | `GET /actions/tests` | [docs](https://docs.currents.dev/api/resources) |
| [Search Spec Files](actions/search-spec-files.md) | `GET /spec-files/:projectId` | [docs](https://docs.currents.dev/resources/api/api-resources/spec-files) |
| [Search Tests](actions/search-tests.md) | `GET /tests/:projectId` | [docs](https://docs.currents.dev/resources/api/api-resources/tests) |
