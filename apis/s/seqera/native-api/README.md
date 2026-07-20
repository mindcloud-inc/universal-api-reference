# Seqera: Native API Reference

A consolidated summary of Seqera's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.seqera.io/platform-api/
- **OpenAPI specification:** https://cloud.seqera.io/openapi/seqera-api-latest.yml
- **API base URL:** `https://api.cloud.seqera.io`

## Authentication

### Bearer Personal Access Token

Seqera Platform API bearer token authentication

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.seqera.io/platform-api/token-list)

## Pagination

Use `max` in the query string to set the page size. Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Run](actions/cancel-run.md) | `POST /ga4gh/wes/v1/runs/:run_id/cancel` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [Create Workspace Participant](actions/create-workspace-participant.md) | `PUT /orgs/:orgId/workspaces/:workspaceId/participants/add` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [Describe Dataset](actions/describe-dataset.md) | `GET /workspaces/:workspaceId/datasets/:datasetId/metadata` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [Describe Pipeline Launch](actions/describe-pipeline-launch.md) | `GET /pipelines/:pipelineId/launch` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [Describe Remote Pipeline Repository](actions/describe-pipeline-repository.md) | `GET /pipelines/info` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [Describe Pipeline Schema](actions/describe-pipeline-schema.md) | `GET /pipelines/:pipelineId/schema` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [Describe Run](actions/describe-run.md) | `GET /ga4gh/wes/v1/runs/:run_id` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [Describe Workspace](actions/describe-workspace.md) | `GET /orgs/:orgId/workspaces/:workspaceId` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [Get Encrypted Credentials](actions/get-encrypted-credentials.md) | `GET /credentials/:credentialsId/keys` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [List Compute Environments](actions/list-compute-environments.md) | `GET /compute-envs` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [List Credentials](actions/list-credentials.md) | `GET /credentials` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [List Data Links](actions/list-data-links.md) | `GET /data-links` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [List Datasets](actions/list-datasets.md) | `GET /workspaces/:workspaceId/datasets` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [List Labels](actions/list-labels.md) | `GET /labels` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [List Organization Workspaces](actions/list-organization-workspaces.md) | `GET /orgs/:orgId/workspaces` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [List Organizations](actions/list-organizations.md) | `GET /orgs` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [List Pipeline Versions](actions/list-pipeline-versions.md) | `GET /pipelines/:pipelineId/versions` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [List Pipelines](actions/list-pipelines.md) | `GET /pipelines` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [List Roles](actions/list-roles.md) | `GET /roles` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [List Runs](actions/list-runs.md) | `GET /ga4gh/wes/v1/runs` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [List SSH Keys](actions/list-ssh-keys.md) | `GET /ssh-keys` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [List Studios](actions/list-studios.md) | `GET /studios` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [List Tokens](actions/list-tokens.md) | `GET /tokens` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [List Workspace Participants](actions/list-workspace-participants.md) | `GET /orgs/:orgId/workspaces/:workspaceId/participants` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [Retrieve Run Status](actions/retrieve-run-status.md) | `GET /ga4gh/wes/v1/runs/:run_id/status` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [Update Workspace Participant Role](actions/update-workspace-participant-role.md) | `PUT /orgs/:orgId/workspaces/:workspaceId/participants/:participantId/role` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [Upload Dataset Version](actions/upload-dataset-version.md) | `POST /workspaces/:workspaceId/datasets/:datasetId/upload` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [Validate Compute Environment Name](actions/validate-compute-environment-name.md) | `GET /compute-envs/validate` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [Validate Credential Name](actions/validate-credential-name.md) | `GET /credentials/validate` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
| [Validate Pipeline Name](actions/validate-pipeline-name.md) | `GET /pipelines/validate` | [docs](https://cloud.seqera.io/openapi/seqera-api-latest.yml) |
