# List Pipelines with Harness

Retrieves pipelines from Harness.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/orgs/:orgIdentifier/projects/:projectIdentifier/pipelines`
- **Base URL:** `https://app.harness.io/gateway`
- **Official documentation:** [List Pipelines](https://apidocs.harness.io/pipelines/list-pipelines)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deployment_type` | query | `string` | no | Deployment type to filter pipelines by. |
| `description` | query | `string` | no | Filter by pipeline description. |
| `env_names` | query | `list<string>` | no | Environment names to filter pipelines by. |
| `filter_identifier` | query | `string` | no | Saved filter identifier. |
| `module` | query | `string` | no | Harness module included in the pipeline. |
| `name` | query | `string` | no | Filter by pipeline name. |
| `order` | query | `string` | no | Sort direction. |
| `pipeline_identifiers` | query | `list<string>` | no | Pipeline identifiers to include. |
| `repository` | query | `string` | no | Repository name to filter pipelines by. |
| `search_term` | query | `string` | no | Filter pipelines matching the search term. |
| `service_names` | query | `list<string>` | no | Service names to filter pipelines by. |
| `sort` | query | `string` | no | Field used for sorting. |
| `tags` | query | `string` | no | Filter by tags using key:value syntax. |
