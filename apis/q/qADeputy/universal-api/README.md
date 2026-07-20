# <img src="https://images.mindcloud.co/apps/icons/qadeputy_1776355025859.jpeg" alt="QADeputy logo" width="28" height="28"> QADeputy: Universal API

QADeputy provides public API access to core QADeputy test management resources, including test runs, test suites, test cases, test results, users, products, and test case statuses.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/qADeputy/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://qadeputy.com/
- **Vendor API docs:** https://apidocs.qadeputy.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Products](actions/list-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Product

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET | Retrieves products from QADeputy. |

### Test Case

| Action | Method | Description |
| --- | --- | --- |
| [Create Test Suite Test Case](actions/create-test-suite-test-case.md) | POST | Creates a test case in a QADeputy test suite. |
| [Get Test Suite Test Case](actions/get-test-suite-test-case.md) | GET | Retrieves a test case from a QADeputy test suite. |
| [List Test Run Test Cases](actions/list-test-run-test-cases.md) | GET | Retrieves test cases in a QADeputy test run. |
| [List Test Suite Test Cases](actions/list-test-suite-test-cases.md) | GET | Retrieves test cases in a QADeputy test suite. |
| [Update Test Run Test Case](actions/update-test-run-test-case.md) | PUT | Updates a test case in a QADeputy test run. |
| [Update Test Suite Test Case](actions/update-test-suite-test-case.md) | PUT | Updates a test case in a QADeputy test suite. |

### Test Case Status

| Action | Method | Description |
| --- | --- | --- |
| [List Test Case Statuses](actions/list-test-case-statuses.md) | GET | Retrieves test case statuses from QADeputy. |

### Test Result

| Action | Method | Description |
| --- | --- | --- |
| [Create Test Result](actions/create-test-result.md) | POST | Creates a test result for a QADeputy test case. |
| [List Test Results](actions/list-test-results.md) | GET | Retrieves test results for a QADeputy test case. |

### Test Run

| Action | Method | Description |
| --- | --- | --- |
| [Create Test Run](actions/create-test-run.md) | POST | Creates a new test run in QADeputy. |
| [Get Test Run](actions/get-test-run.md) | GET | Retrieves a test run from QADeputy. |
| [List Test Runs](actions/list-test-runs.md) | GET | Retrieves test runs from QADeputy. |
| [Update Test Run](actions/update-test-run.md) | PUT | Updates an existing test run in QADeputy. |

### Test Suite

| Action | Method | Description |
| --- | --- | --- |
| [Create Test Suite](actions/create-test-suite.md) | POST | Creates a new test suite in QADeputy. |
| [Get Test Suite](actions/get-test-suite.md) | GET | Retrieves a test suite from QADeputy. |
| [List Test Suites](actions/list-test-suites.md) | GET | Retrieves test suites from QADeputy. |
| [Update Test Suite](actions/update-test-suite.md) | PUT | Updates an existing test suite in QADeputy. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from QADeputy. |

