# Harness: Native API Reference

A consolidated summary of Harness's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.harness.io/
- **API base URL:** `https://app.harness.io/gateway`

## Authentication

### API Key

Authenticate Harness requests with an x-api-key token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://developer.harness.io/docs/platform/automation/api/api-quickstart/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Connector](actions/create-connector.md) | `POST /ng/api/connectors` | [docs](https://apidocs.harness.io/connectors/createconnector) |
| [Create Input Set](actions/create-input-set.md) | `POST https://app.harness.io/pipeline/api/inputSets?accountIdentifier=:accountIdentifier&orgIdentifier=:orgIdentifier&projectIdentifier=:projectIdentifier&pipelineIdentifier=:pipelineIdentifier` | [docs](https://apidocs.harness.io/input-sets/create-input-set) |
| [Create Pipeline](actions/create-pipeline.md) | `POST https://app.harness.io/pipeline/api/pipelines/v2?accountIdentifier=:accountIdentifier&orgIdentifier=:orgIdentifier&projectIdentifier=:projectIdentifier` | [docs](https://apidocs.harness.io/pipelines/create-pipeline) |
| [Delete Connector](actions/delete-connector.md) | `DELETE /ng/api/connectors/:identifier` | [docs](https://apidocs.harness.io/connectors/deleteconnector) |
| [Delete Input Set](actions/delete-input-set.md) | `DELETE https://app.harness.io/pipeline/api/inputSets/:inputSetIdentifier?accountIdentifier=:accountIdentifier&orgIdentifier=:orgIdentifier&projectIdentifier=:projectIdentifier&pipelineIdentifier=:pipelineIdentifier` | [docs](https://apidocs.harness.io/input-sets/delete-input-set) |
| [Delete Pipeline](actions/delete-pipeline.md) | `DELETE https://app.harness.io/pipeline/api/pipelines/:pipelineIdentifier?accountIdentifier=:accountIdentifier&orgIdentifier=:orgIdentifier&projectIdentifier=:projectIdentifier` | [docs](https://apidocs.harness.io/pipelines/delete-pipeline) |
| [Execute Pipeline With Input Set References](actions/execute-pipeline-with-input-set-references.md) | `POST https://app.harness.io/pipeline/api/pipeline/execute/:pipelineIdentifier/inputSetList?accountIdentifier=:accountIdentifier&orgIdentifier=:orgIdentifier&projectIdentifier=:projectIdentifier` | [docs](https://apidocs.harness.io/pipeline-execution/postpipelineexecutewithinputsetyaml) |
| [Get Account](actions/get-account.md) | `GET /ng/api/accounts/:accountIdentifier` | [docs](https://apidocs.harness.io/accounts/getaccountng) |
| [Get Current User Info](actions/get-current-user-info.md) | `GET /ng/api/user/currentUser` | [docs](https://apidocs.harness.io/user/getcurrentuserinfo) |
| [List Connectors](actions/list-connectors.md) | `GET /ng/api/connectors` | [docs](https://apidocs.harness.io/connectors/getconnectorlist) |
| [List Pipelines](actions/list-pipelines.md) | `GET /v1/orgs/:orgIdentifier/projects/:projectIdentifier/pipelines` | [docs](https://apidocs.harness.io/pipelines/list-pipelines) |
| [List Service Accounts](actions/list-service-accounts.md) | `GET /ng/api/serviceaccount` | [docs](https://apidocs.harness.io/service-account/listserviceaccount) |
| [List Services](actions/list-services.md) | `GET /ng/api/servicesV2` | [docs](https://apidocs.harness.io/services/getservicelist) |
| [List Users](actions/list-users.md) | `POST /ng/api/user/batch` | [docs](https://apidocs.harness.io/user/getusers) |
| [Validate Token](actions/validate-token.md) | `POST /ng/api/token/validate` | [docs](https://apidocs.harness.io/token/validatetoken) |
