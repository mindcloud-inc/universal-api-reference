# <img src="https://images.mindcloud.co/apps/icons/images-9_1775771337080.png" alt="Currents logo" width="28" height="28"> Currents: Universal API

Currents API wrapper for test observability, runs, instances, spec files, test results, and Currents Actions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/currents/latest
- **Category:** IT Operations / Observability
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://currents.dev/
- **Vendor API docs:** https://docs.currents.dev/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/currents/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Actions

| Action | Method | Description |
| --- | --- | --- |
| [Get Action](actions/get-action.md) | GET |  |
| [List Actions](actions/list-actions.md) | GET |  |
| [List Active Actions](actions/list-active-actions.md) | GET |  |
| [List Disabled Actions](actions/list-disabled-actions.md) | GET |  |
| [Search Actions](actions/search-actions.md) | GET |  |

### Builds

| Action | Method | Description |
| --- | --- | --- |
| [Get Instance](actions/get-instance.md) | GET |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [List Failing Spec Files](actions/list-failing-spec-files.md) | GET |  |
| [List Slow Spec Files](actions/list-slow-spec-files.md) | GET |  |
| [List Spec Files](actions/list-spec-files.md) | GET |  |
| [Search Spec Files](actions/search-spec-files.md) | GET |  |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET |  |
| [Get Project Insights](actions/get-project-insights.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |

### Signature Requests

| Action | Method | Description |
| --- | --- | --- |
| [Generate Test Signature](actions/generate-test-signature.md) | POST |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Affected Test Executions](actions/get-affected-test-executions.md) | GET |  |
| [Get Test Results](actions/get-test-results.md) | GET |  |
| [List Action Executions](actions/list-action-executions.md) | GET |  |
| [List Action Tests](actions/list-action-tests.md) | GET |  |
| [List Affected Tests](actions/list-affected-tests.md) | GET |  |
| [List Failing Tests](actions/list-failing-tests.md) | GET |  |
| [List Flaky Tests](actions/list-flaky-tests.md) | GET |  |
| [List Quarantined Tests](actions/list-quarantined-tests.md) | GET |  |
| [List Skipped Tests](actions/list-skipped-tests.md) | GET |  |
| [List Slow Tests](actions/list-slow-tests.md) | GET |  |
| [List Tagged Tests](actions/list-tagged-tests.md) | GET |  |
| [List Tests](actions/list-tests.md) | GET |  |
| [Search Affected Tests](actions/search-affected-tests.md) | GET |  |
| [Search Tests](actions/search-tests.md) | GET |  |

### Workflow Runs

| Action | Method | Description |
| --- | --- | --- |
| [Get Run](actions/get-run.md) | GET |  |
| [List Runs](actions/list-runs.md) | GET |  |

