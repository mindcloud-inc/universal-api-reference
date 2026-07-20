# Google Cloud Document AI: Native API Reference

A consolidated summary of Google Cloud Document AI's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://cloud.google.com/document-ai/docs/reference/rest/v1
- **OpenAPI specification:** https://documentai.googleapis.com/$discovery/rest?version=v1
- **API base URL:** `https://documentai.googleapis.com`

## Authentication

### Google OAuth2

Connect with Google OAuth 2.0 using the cloud-platform scope for Google Cloud Document AI.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.google.com/o/oauth2/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth2.googleapis.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `https://www.googleapis.com/auth/cloud-platform`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://oauth2.googleapis.com/token.

[Official authentication documentation](https://developers.google.com/identity/protocols/oauth2/web-server)

### Service Account

Authenticate Google Cloud Document AI with a Google Cloud service account private key.

### Credentials

- **Project ID:** `project` · required · The Google Cloud project ID that contains the Document AI resources this connection should access.
- **Client Email:** `clientEmail` · required · The client_email value from the service account key JSON file.
- **Private Key ID:** `privateKeyId` · optional · Optional legacy field from the service account key JSON file. The Google auth SDK can mint Document AI access tokens with only project ID, client email, and private key.
- **Private Key:** `privateKeySecret` · required · The private_key value from the service account key JSON file. MindCloud uses it only to sign short-lived Google OAuth JWT assertions.

[Official authentication documentation](https://developers.google.com/identity/protocols/oauth2/service-account)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectsId` | path | `string` | yes | Google Cloud project ID from paths like projects/{project}/locations/{location}. |
| `locationsId` | path | `string` | yes | Document AI location ID, such as us or eu. |

Responses from this API use JSON.

## Pagination

Use `pageSize` in the query string to set the page size (default 50; accepted range 1–100). Use `pageToken` in the query string as the pagination cursor; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Process Documents With Processor](actions/batch-process-documents-with-processor.md) | `POST /v1/projects/:projectsId/locations/:locationsId/processors/:processorsId:batchProcess` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors/batchProcess) |
| [Batch Process Documents With Processor Version](actions/batch-process-documents-with-processor-version.md) | `POST /v1/projects/:projectsId/locations/:locationsId/processors/:processorsId/processorVersions/:processorVersionsId:batchProcess` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors.processorVersions/batchProcess) |
| [Cancel Location Operation](actions/cancel-location-operation.md) | `POST /v1/projects/:projectsId/locations/:locationsId/operations/:operationsId:cancel` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.operations/cancel) |
| [Create Processor](actions/create-processor.md) | `POST /v1/projects/:projectsId/locations/:locationsId/processors` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors/create) |
| [Create Schema](actions/create-schema.md) | `POST /v1/projects/:projectsId/locations/:locationsId/schemas` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.schemas/create) |
| [Create Schema Version](actions/create-schema-version.md) | `POST /v1/projects/:projectsId/locations/:locationsId/schemas/:schemasId/schemaVersions` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.schemas.schemaVersions/create) |
| [Delete Processor](actions/delete-processor.md) | `DELETE /v1/projects/:projectsId/locations/:locationsId/processors/:processorsId` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors/delete) |
| [Delete Processor Version](actions/delete-processor-version.md) | `DELETE /v1/projects/:projectsId/locations/:locationsId/processors/:processorsId/processorVersions/:processorVersionsId` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors.processorVersions/delete) |
| [Delete Schema](actions/delete-schema.md) | `DELETE /v1/projects/:projectsId/locations/:locationsId/schemas/:schemasId` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.schemas/delete) |
| [Delete Schema Version](actions/delete-schema-version.md) | `DELETE /v1/projects/:projectsId/locations/:locationsId/schemas/:schemasId/schemaVersions/:schemaVersionsId` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.schemas.schemaVersions/delete) |
| [Deploy Processor Version](actions/deploy-processor-version.md) | `POST /v1/projects/:projectsId/locations/:locationsId/processors/:processorsId/processorVersions/:processorVersionsId:deploy` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors.processorVersions/deploy) |
| [Disable Processor](actions/disable-processor.md) | `POST /v1/projects/:projectsId/locations/:locationsId/processors/:processorsId:disable` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors/disable) |
| [Enable Processor](actions/enable-processor.md) | `POST /v1/projects/:projectsId/locations/:locationsId/processors/:processorsId:enable` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors/enable) |
| [Evaluate Processor Version](actions/evaluate-processor-version.md) | `POST /v1/projects/:projectsId/locations/:locationsId/processors/:processorsId/processorVersions/:processorVersionsId:evaluateProcessorVersion` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors.processorVersions/evaluateProcessorVersion) |
| [Fetch Processor Types](actions/fetch-processor-types.md) | `GET /v1/projects/:projectsId/locations/:locationsId:fetchProcessorTypes` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations/fetchProcessorTypes) |
| [Generate Schema Version](actions/generate-schema-version.md) | `POST /v1/projects/:projectsId/locations/:locationsId/schemas/:schemasId/schemaVersions:generate` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.schemas.schemaVersions/generate) |
| [Get Location](actions/get-location.md) | `GET /v1/projects/:projectsId/locations/:locationsId` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations/get) |
| [Get Location Operation](actions/get-location-operation.md) | `GET /v1/projects/:projectsId/locations/:locationsId/operations/:operationsId` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.operations/get) |
| [Get Processor](actions/get-processor.md) | `GET /v1/projects/:projectsId/locations/:locationsId/processors/:processorsId` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors/get) |
| [Get Processor Type](actions/get-processor-type.md) | `GET /v1/projects/:projectsId/locations/:locationsId/processorTypes/:processorTypesId` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processorTypes/get) |
| [Get Processor Version](actions/get-processor-version.md) | `GET /v1/projects/:projectsId/locations/:locationsId/processors/:processorsId/processorVersions/:processorVersionsId` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors.processorVersions/get) |
| [Get Processor Version Evaluation](actions/get-processor-version-evaluation.md) | `GET /v1/projects/:projectsId/locations/:locationsId/processors/:processorsId/processorVersions/:processorVersionsId/evaluations/:evaluationsId` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors.processorVersions.evaluations/get) |
| [Get Schema](actions/get-schema.md) | `GET /v1/projects/:projectsId/locations/:locationsId/schemas/:schemasId` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.schemas/get) |
| [Get Schema Version](actions/get-schema-version.md) | `GET /v1/projects/:projectsId/locations/:locationsId/schemas/:schemasId/schemaVersions/:schemaVersionsId` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.schemas.schemaVersions/get) |
| [List Location Operations](actions/list-location-operations.md) | `GET /v1/projects/:projectsId/locations/:locationsId/operations` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.operations/list) |
| [List Locations](actions/list-locations.md) | `GET /v1/projects/:projectsId/locations` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations/list) |
| [List Processor Types](actions/list-processor-types.md) | `GET /v1/projects/:projectsId/locations/:locationsId/processorTypes` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processorTypes/list) |
| [List Processor Version Evaluations](actions/list-processor-version-evaluations.md) | `GET /v1/projects/:projectsId/locations/:locationsId/processors/:processorsId/processorVersions/:processorVersionsId/evaluations` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors.processorVersions.evaluations/list) |
| [List Processor Versions](actions/list-processor-versions.md) | `GET /v1/projects/:projectsId/locations/:locationsId/processors/:processorsId/processorVersions` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors.processorVersions/list) |
| [List Processors](actions/list-processors.md) | `GET /v1/projects/:projectsId/locations/:locationsId/processors` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors/list) |
| [List Schema Versions](actions/list-schema-versions.md) | `GET /v1/projects/:projectsId/locations/:locationsId/schemas/:schemasId/schemaVersions` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.schemas.schemaVersions/list) |
| [List Schemas](actions/list-schemas.md) | `GET /v1/projects/:projectsId/locations/:locationsId/schemas` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.schemas/list) |
| [Process Document With Processor](actions/process-document-with-processor.md) | `POST /v1/projects/:projectsId/locations/:locationsId/processors/:processorsId:process` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors/process) |
| [Process Document With Processor Version](actions/process-document-with-processor-version.md) | `POST /v1/projects/:projectsId/locations/:locationsId/processors/:processorsId/processorVersions/:processorVersionsId:process` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors.processorVersions/process) |
| [Review Document With Human Review Config](actions/review-document-with-human-review-config.md) | `POST /v1/projects/:projectsId/locations/:locationsId/processors/:processorsId/humanReviewConfig:reviewDocument` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors.humanReviewConfig/reviewDocument) |
| [Set Default Processor Version](actions/set-default-processor-version.md) | `POST /v1/projects/:projectsId/locations/:locationsId/processors/:processorsId:setDefaultProcessorVersion` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors/setDefaultProcessorVersion) |
| [Train Processor Version](actions/train-processor-version.md) | `POST /v1/projects/:projectsId/locations/:locationsId/processors/:processorsId/processorVersions:train` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors.processorVersions/train) |
| [Undeploy Processor Version](actions/undeploy-processor-version.md) | `POST /v1/projects/:projectsId/locations/:locationsId/processors/:processorsId/processorVersions/:processorVersionsId:undeploy` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors.processorVersions/undeploy) |
| [Update Schema](actions/update-schema.md) | `PATCH /v1/projects/:projectsId/locations/:locationsId/schemas/:schemasId` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.schemas/patch) |
| [Update Schema Version](actions/update-schema-version.md) | `PATCH /v1/projects/:projectsId/locations/:locationsId/schemas/:schemasId/schemaVersions/:schemaVersionsId` | [docs](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.schemas.schemaVersions/patch) |
