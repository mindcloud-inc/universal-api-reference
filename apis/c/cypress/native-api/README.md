# Cypress: Native API Reference

A consolidated summary of Cypress's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.cypress.io/cloud/integrations/data-extract-api
- **API base URL:** `https://cloud.cypress.io/enterprise-reporting/report`

## Authentication

### Cypress API Key

Use your Cypress organization API key. Cypress Data Extract requests require the key on every request as the documented query parameter `token`.

### Credentials

- **API Key:** `apiKey` · required · Your Cypress organization API key for the Enterprise Reporting Data Extract API.

[Official authentication documentation](https://docs.cypress.io/cloud/integrations/data-extract-api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `branch` | query | `string` | no | Optional git branch name filter. Repeat this query parameter to filter multiple branches. |
| `end_date` | query | `string` | no | Optional end date in YYYY-MM-DD format. Cypress requires start_date to be before the current time and before any supplied end_date. |
| `projects` | query | `string` | no | Optional Cypress project IDs to filter the report. Repeat this query parameter to filter multiple projects. |
| `spec` | query | `string` | no | Optional spec path filter for spec-level and test-level reports. |
| `start_date` | query | `string` | yes | Start date in YYYY-MM-DD format. Cypress requires this value for report queries and it must be within the last 365 days. |
| `tags` | query | `string` | no | Optional run tags filter. Repeat this query parameter to filter multiple tags. |
| `test_name` | query | `string` | no | Optional test name filter for test-level reports. |

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Accessibility Score Details](actions/accessibility-score-details.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#Accessibility-score-details) |
| [Accessibility Score Per Project](actions/accessibility-score-per-project.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#Accessibility-score-per-project) |
| [Accessibility Score Per Project Over Time](actions/accessibility-score-per-project-over-time.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#Accessibility-score-per-project-over-time) |
| [Average Run Duration Over Time](actions/average-run-duration-over-time.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#Average-run-duration-over-time) |
| [Browser Versions Tested](actions/browser-versions-tested.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#Browser-versions-tested) |
| [Browser Versions Tested Over Time](actions/browser-versions-tested-over-time.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#Browser-versions-tested-over-time) |
| [Browser Versions Tested Per Project Over Time](actions/browser-versions-tested-per-project-over-time.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#Browser-versions-tested-per-project-over-time) |
| [Browsers Tested](actions/browsers-tested.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#Browsers-tested) |
| [Cypress Run Versions](actions/cypress-run-versions.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#Cypress-run-versions) |
| [Cypress Run Versions Over Time](actions/cypress-run-versions-over-time.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#Cypress-run-versions-over-time) |
| [Cypress Run Versions Per Project Over Time](actions/cypress-run-versions-per-project-over-time.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#Cypress-run-versions-per-project-over-time) |
| [Cypress Test Suite Over Time](actions/cypress-test-suite-over-time.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#Cypress-test-suite-over-time) |
| [Cypress Test Suite Size](actions/cypress-test-suite-size.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#Cypress-test-suite-size) |
| [Cypress Test Types](actions/cypress-test-types.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#Cypress-test-types) |
| [Flaky Rate Per Project](actions/flaky-rate-per-project.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#Flaky-rate-per-project) |
| [Flaky Rate Per Project Over Time](actions/flaky-rate-per-project-over-time.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#Flaky-rate-per-project-over-time) |
| [List Projects](actions/list-projects.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#Project-list) |
| [Project Test Count And Status](actions/project-test-count-and-status.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#Project-test-count-and-status) |
| [Status By Run](actions/status-by-run.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#Status-by-run) |
| [Status By Run Over Time](actions/status-by-run-over-time.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#Status-by-run-over-time) |
| [Status By Spec](actions/status-by-spec.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#Status-by-spec) |
| [Status By Spec Over Time](actions/status-by-spec-over-time.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#Status-by-spec-over-time) |
| [Status By Test Run](actions/status-by-test-run.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#Status-by-test-run) |
| [Status By Test Run Over Time](actions/status-by-test-run-over-time.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#Status-by-test-run-over-time) |
| [Test Flake Detail Over Time](actions/test-flake-detail-over-time.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#Test-flake-detail-over-time) |
| [Tests Per Project](actions/tests-per-project.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#Tests-per-project) |
| [Tests Per Project Over Time](actions/tests-per-project-over-time.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#Tests-per-project-over-time) |
| [UI Coverage Details](actions/u-i-coverage-details.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#UI-Coverage-details) |
| [UI Coverage Per Project](actions/u-i-coverage-per-project.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#UI-Coverage-per-project) |
| [UI Coverage Per Project Over Time](actions/u-i-coverage-per-project-over-time.md) | `GET /` | [docs](https://docs.cypress.io/cloud/integrations/data-extract-api#UI-Coverage-per-project-over-time) |
