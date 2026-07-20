# <img src="https://images.mindcloud.co/apps/icons/cypress_1775506280079.png" alt="Cypress logo" width="28" height="28"> Cypress: Universal API

Extract Cypress Cloud enterprise reporting data such as project usage, run status, flake trends, browser coverage, UI coverage, and accessibility metrics through the documented Data Extract API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cypress/latest
- **Category:** IT Operations / Observability
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.cypress.io
- **Vendor API docs:** https://docs.cypress.io/cloud/integrations/data-extract-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cypress/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Accessibility Score Details

| Action | Method | Description |
| --- | --- | --- |
| [Accessibility Score Details](actions/accessibility-score-details.md) | GET | Retrieves accessibility score details from Cypress Cloud. |

### Accessibility Score Per Project

| Action | Method | Description |
| --- | --- | --- |
| [Accessibility Score Per Project](actions/accessibility-score-per-project.md) | GET | Retrieves accessibility scores per project from Cypress Cloud. |

### Accessibility Score Per Project Over Time

| Action | Method | Description |
| --- | --- | --- |
| [Accessibility Score Per Project Over Time](actions/accessibility-score-per-project-over-time.md) | GET | Retrieves accessibility scores per project over time from Cypress Cloud. |

### Average Run Duration Over Time

| Action | Method | Description |
| --- | --- | --- |
| [Average Run Duration Over Time](actions/average-run-duration-over-time.md) | GET | Retrieves average run durations over time from Cypress Cloud. |

### Browser Versions Tested

| Action | Method | Description |
| --- | --- | --- |
| [Browser Versions Tested](actions/browser-versions-tested.md) | GET | Retrieves tested browser versions from Cypress Cloud. |

### Browser Versions Tested Over Time

| Action | Method | Description |
| --- | --- | --- |
| [Browser Versions Tested Over Time](actions/browser-versions-tested-over-time.md) | GET | Retrieves tested browser versions over time from Cypress Cloud. |

### Browser Versions Tested Per Project Over Time

| Action | Method | Description |
| --- | --- | --- |
| [Browser Versions Tested Per Project Over Time](actions/browser-versions-tested-per-project-over-time.md) | GET | Retrieves project-level browser versions over time from Cypress Cloud. |

### Browsers Tested

| Action | Method | Description |
| --- | --- | --- |
| [Browsers Tested](actions/browsers-tested.md) | GET | Retrieves tested browsers from Cypress Cloud. |

### Cypress Project

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | GET | Retrieves recorded projects from Cypress Cloud. |

### Cypress Run Versions

| Action | Method | Description |
| --- | --- | --- |
| [Cypress Run Versions](actions/cypress-run-versions.md) | GET | Retrieves Cypress run versions from Cypress Cloud. |

### Cypress Run Versions Over Time

| Action | Method | Description |
| --- | --- | --- |
| [Cypress Run Versions Over Time](actions/cypress-run-versions-over-time.md) | GET | Retrieves Cypress run versions over time from Cypress Cloud. |

### Cypress Run Versions Per Project Over Time

| Action | Method | Description |
| --- | --- | --- |
| [Cypress Run Versions Per Project Over Time](actions/cypress-run-versions-per-project-over-time.md) | GET | Retrieves project-level Cypress run versions over time from Cypress Cloud. |

### Cypress Test Suite Over Time

| Action | Method | Description |
| --- | --- | --- |
| [Cypress Test Suite Over Time](actions/cypress-test-suite-over-time.md) | GET | Retrieves Cypress test suite growth over time from Cypress Cloud. |

### Cypress Test Suite Size

| Action | Method | Description |
| --- | --- | --- |
| [Cypress Test Suite Size](actions/cypress-test-suite-size.md) | GET | Retrieves Cypress test suite size data from Cypress Cloud. |

### Cypress Test Types

| Action | Method | Description |
| --- | --- | --- |
| [Cypress Test Types](actions/cypress-test-types.md) | GET | Retrieves Cypress test type adoption data from Cypress Cloud. |

### Flaky Rate Per Project

| Action | Method | Description |
| --- | --- | --- |
| [Flaky Rate Per Project](actions/flaky-rate-per-project.md) | GET | Retrieves flaky rates per project from Cypress Cloud. |

### Flaky Rate Per Project Over Time

| Action | Method | Description |
| --- | --- | --- |
| [Flaky Rate Per Project Over Time](actions/flaky-rate-per-project-over-time.md) | GET | Retrieves flaky rates per project over time from Cypress Cloud. |

### Project Test Count And Status

| Action | Method | Description |
| --- | --- | --- |
| [Project Test Count And Status](actions/project-test-count-and-status.md) | GET | Retrieves project test counts and statuses from Cypress Cloud. |

### Run Status Over Time

| Action | Method | Description |
| --- | --- | --- |
| [Status By Run Over Time](actions/status-by-run-over-time.md) | GET | Retrieves run status rates over time from Cypress Cloud. |

### Run Status Summary

| Action | Method | Description |
| --- | --- | --- |
| [Status By Run](actions/status-by-run.md) | GET | Retrieves run status rates from Cypress Cloud. |

### Spec Status Over Time

| Action | Method | Description |
| --- | --- | --- |
| [Status By Spec Over Time](actions/status-by-spec-over-time.md) | GET | Retrieves spec status rates over time from Cypress Cloud. |

### Spec Status Summary

| Action | Method | Description |
| --- | --- | --- |
| [Status By Spec](actions/status-by-spec.md) | GET | Retrieves spec status rates from Cypress Cloud. |

### Test Flake Detail Over Time

| Action | Method | Description |
| --- | --- | --- |
| [Test Flake Detail Over Time](actions/test-flake-detail-over-time.md) | GET | Retrieves test flake details over time from Cypress Cloud. |

### Test Status Over Time

| Action | Method | Description |
| --- | --- | --- |
| [Status By Test Run Over Time](actions/status-by-test-run-over-time.md) | GET | Retrieves individual test status rates over time from Cypress Cloud. |

### Test Status Summary

| Action | Method | Description |
| --- | --- | --- |
| [Status By Test Run](actions/status-by-test-run.md) | GET | Retrieves individual test status rates from Cypress Cloud. |

### Tests Per Project

| Action | Method | Description |
| --- | --- | --- |
| [Tests Per Project](actions/tests-per-project.md) | GET | Retrieves the tests per project report from Cypress Cloud. |

### Tests Per Project Over Time

| Action | Method | Description |
| --- | --- | --- |
| [Tests Per Project Over Time](actions/tests-per-project-over-time.md) | GET | Retrieves tests per project over time from Cypress Cloud. |

### Ui Coverage Details

| Action | Method | Description |
| --- | --- | --- |
| [UI Coverage Details](actions/u-i-coverage-details.md) | GET | Retrieves UI coverage details from Cypress Cloud. |

### Ui Coverage Per Project

| Action | Method | Description |
| --- | --- | --- |
| [UI Coverage Per Project](actions/u-i-coverage-per-project.md) | GET | Retrieves UI coverage per project from Cypress Cloud. |

### Ui Coverage Per Project Over Time

| Action | Method | Description |
| --- | --- | --- |
| [UI Coverage Per Project Over Time](actions/u-i-coverage-per-project-over-time.md) | GET | Retrieves UI coverage per project over time from Cypress Cloud. |

