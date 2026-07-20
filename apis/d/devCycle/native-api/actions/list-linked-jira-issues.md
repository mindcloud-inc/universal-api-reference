# List Linked Jira Issues with DevCycle

Retrieves linked Jira issues for a feature from DevCycle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project/features/:feature/integrations/jira/issues`
- **Base URL:** `https://api.devcycle.com`
- **Official documentation:** [List Linked Jira Issues](https://docs.devcycle.com/management-api/#tag/Deprecated-Features-v1/operation/FeaturesController_findAllLinkedIssues_v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feature` | path | `string` | no | Feature key. |
| `project` | path | `string` | no | Project key. |
