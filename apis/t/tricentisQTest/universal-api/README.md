# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-04-15-as-16_1776283141443.png" alt="Tricentis qTest logo" width="28" height="28"> Tricentis qTest: Universal API

Tricentis qTest is a test management platform for projects, requirements, test cases, test runs, defects, attachments, comments, and execution results.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tricentisQTest/latest
- **Category:** Productivity / Project Management
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.tricentis.com/products/qtest-test-management
- **Vendor API docs:** https://docs.tricentis.com/qtest-saas/content/apis/overview/how_to_use_interactive_api_documentation.htm

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Admin Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Admin Profile](actions/get-current-admin-profile.md) | GET | Retrieves the current admin profile from Tricentis qTest. |

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Search Attachments](actions/search-attachments.md) | GET | Finds attachments in Tricentis qTest by object criteria. |

### Authentication System

| Action | Method | Description |
| --- | --- | --- |
| [List Authentication Systems](actions/list-authentication-systems.md) | GET | Retrieves authentication systems from Tricentis qTest. |

### Build

| Action | Method | Description |
| --- | --- | --- |
| [Get Build](actions/get-build.md) | GET | Retrieves a build from Tricentis qTest. |
| [List Builds](actions/list-builds.md) | GET | Retrieves available builds from Tricentis qTest. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Query Comments](actions/query-comments.md) | GET | Finds comments in Tricentis qTest by query criteria. |

### Defect

| Action | Method | Description |
| --- | --- | --- |
| [Get Defect](actions/get-defect.md) | GET | Retrieves a defect from Tricentis qTest. |
| [List Recently Updated Defects](actions/list-recently-updated-defects.md) | GET | Retrieves recently updated defects from Tricentis qTest. |

### Defect Comment

| Action | Method | Description |
| --- | --- | --- |
| [Get Defect Comment](actions/get-defect-comment.md) | GET | Retrieves a defect comment from Tricentis qTest. |
| [List Defect Comments](actions/list-defect-comments.md) | GET | Retrieves defect comments from Tricentis qTest. |

### Field Allowed Value

| Action | Method | Description |
| --- | --- | --- |
| [List Field Allowed Values](actions/list-field-allowed-values.md) | GET | Retrieves allowed field values from Tricentis qTest. |

### Jira Connection

| Action | Method | Description |
| --- | --- | --- |
| [List Jira Connections](actions/list-jira-connections.md) | GET | Retrieves Jira connections from Tricentis qTest. |

### Linked Artifact

| Action | Method | Description |
| --- | --- | --- |
| [List Linked Artifacts](actions/list-linked-artifacts.md) | GET | Retrieves linked artifacts from Tricentis qTest. |

### Module

| Action | Method | Description |
| --- | --- | --- |
| [Get Module](actions/get-module.md) | GET | Retrieves a module from Tricentis qTest. |
| [List Modules](actions/list-modules.md) | GET | Retrieves available modules from Tricentis qTest. |

### Object Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Object Field](actions/get-object-field.md) | GET | Retrieves an object field from Tricentis qTest. |
| [List Object Fields](actions/list-object-fields.md) | GET | Retrieves object fields from Tricentis qTest. |

### Object History

| Action | Method | Description |
| --- | --- | --- |
| [Query Object Histories](actions/query-object-histories.md) | GET | Finds object histories in Tricentis qTest by query criteria. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Tricentis qTest. |
| [List Projects](actions/list-projects.md) | GET | Retrieves available projects from Tricentis qTest. |
| [Search Projects](actions/search-projects.md) | GET | Finds projects in Tricentis qTest by search criteria. |

### Project Object

| Action | Method | Description |
| --- | --- | --- |
| [Search Project Objects](actions/search-project-objects.md) | GET | Finds project objects in Tricentis qTest by query criteria. |

### Release

| Action | Method | Description |
| --- | --- | --- |
| [Get Release](actions/get-release.md) | GET | Retrieves a release from Tricentis qTest. |
| [List Releases](actions/list-releases.md) | GET | Retrieves available releases from Tricentis qTest. |

### Requirement

| Action | Method | Description |
| --- | --- | --- |
| [Get Requirement](actions/get-requirement.md) | GET | Retrieves a requirement from Tricentis qTest. |
| [List Requirements](actions/list-requirements.md) | GET | Retrieves available requirements from Tricentis qTest. |

### Requirement Defect

| Action | Method | Description |
| --- | --- | --- |
| [List Requirement Defects](actions/list-requirement-defects.md) | GET | Retrieves requirement defects from Tricentis qTest. |

### Requirement Test Run

| Action | Method | Description |
| --- | --- | --- |
| [List Requirement Test Runs](actions/list-requirement-test-runs.md) | GET | Retrieves requirement test runs from Tricentis qTest. |

### Requirement Trace Matrix Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Requirement Trace Matrix Report](actions/get-requirement-trace-matrix-report.md) | GET | Retrieves a requirement trace matrix report from Tricentis qTest. |

### Test Case

| Action | Method | Description |
| --- | --- | --- |
| [Get Test Case](actions/get-test-case.md) | GET | Retrieves a test case from Tricentis qTest. |
| [List Test Cases](actions/list-test-cases.md) | GET | Retrieves test cases from Tricentis qTest. |

### Test Case Version

| Action | Method | Description |
| --- | --- | --- |
| [List Test Case Versions](actions/list-test-case-versions.md) | GET | Retrieves test case versions from Tricentis qTest. |

### Test Log

| Action | Method | Description |
| --- | --- | --- |
| [List Test Logs](actions/list-test-logs.md) | GET | Retrieves test logs from Tricentis qTest. |

### Test Run

| Action | Method | Description |
| --- | --- | --- |
| [Get Test Run](actions/get-test-run.md) | GET | Retrieves a test run from Tricentis qTest. |
| [List Test Runs](actions/list-test-runs.md) | GET | Retrieves test runs from Tricentis qTest. |

### Test Run Status

| Action | Method | Description |
| --- | --- | --- |
| [List Test Run Statuses](actions/list-test-run-statuses.md) | GET | Retrieves test run statuses from Tricentis qTest. |

### Test Step

| Action | Method | Description |
| --- | --- | --- |
| [List Test Steps](actions/list-test-steps.md) | GET | Retrieves test steps from Tricentis qTest. |

### Test Suite

| Action | Method | Description |
| --- | --- | --- |
| [List Test Suites](actions/list-test-suites.md) | GET | Retrieves test suites from Tricentis qTest. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Tricentis qTest. |

### User Group

| Action | Method | Description |
| --- | --- | --- |
| [List User Groups](actions/list-user-groups.md) | GET | Retrieves user groups from Tricentis qTest. |

