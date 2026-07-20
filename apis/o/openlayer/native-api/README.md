# Openlayer: Native API Reference

A consolidated summary of Openlayer's API configuration and 51 documented operations, with links to official documentation.

- **Official docs:** https://api.openlayer.com/v1/openapi.json
- **API base URL:** `https://api.openlayer.com/v1`

## Authentication

### API Key

Openlayer uses a single bearer API key sent as Authorization: Bearer <API_KEY>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.openlayer.com/v1/openapi.json)

## Endpoints (51 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Inference Pipeline](actions/create-inference-pipeline.md) | `POST /projects/:projectId/inference-pipelines` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [Create Project User Tag](actions/create-project-user-tag.md) | `POST /projects/:projectId/user-tags` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [Create Project Version](actions/create-project-version.md) | `POST /projects/:projectId/versions` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [Create Storage Upload URL](actions/create-storage-upload-url.md) | `POST /storage/presigned-url` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [Delete Project User Tag](actions/delete-project-user-tag.md) | `DELETE /projects/:projectId/user-tags/:tagId` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [Export Version Data](actions/export-version-data.md) | `POST /versions/:versionId/export` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [Get Build Info](actions/get-build-info.md) | `GET /diagnostics/build-info` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [Get Framework](actions/get-framework.md) | `GET /frameworks/:frameworkId` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [Get Framework Document](actions/get-framework-document.md) | `GET /frameworks/:frameworkId/documents/:documentId` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [Get Framework Project Rule Stats](actions/get-framework-project-rule-stats.md) | `GET /frameworks/:frameworkId/project-rule-stats` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [Get Inference Pipeline](actions/get-inference-pipeline.md) | `GET /inference-pipelines/:inferencePipelineId` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [Get Inference Pipeline Graph Data](actions/get-inference-pipeline-graph-data.md) | `GET /inference-pipelines/:inferencePipelineId/graph-data` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [Get Inference Pipeline Session](actions/get-inference-pipeline-session.md) | `GET /inference-pipelines/:inferencePipelineId/session` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [Get Inference Pipeline User](actions/get-inference-pipeline-user.md) | `GET /inference-pipelines/:inferencePipelineId/user` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [Get Profile](actions/get-profile.md) | `GET /me` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [Get Project Version Upload URL](actions/get-project-version-upload-url.md) | `GET /projects/:projectId/versions/presigned-url` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [Get Rule](actions/get-rule.md) | `GET /rules/:ruleId` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [Get Rule Result](actions/get-rule-result.md) | `GET /rule-results/:ruleResultId` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [Get Storage Download URL](actions/get-storage-download-url.md) | `GET /storage/presigned-url` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [Get Version](actions/get-version.md) | `GET /versions/:versionId` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [Get Workspace](actions/get-workspace.md) | `GET /workspaces/:workspaceId` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [Get Workspace Public Key](actions/get-workspace-public-key.md) | `GET /workspaces/:workspaceId/public-key` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [Get Workspace Rule Stats](actions/get-workspace-rule-stats.md) | `GET /workspaces/:workspaceId/rule-stats` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [Health Check](actions/health-check.md) | `GET /diagnostics/health-check` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [List Framework Documents](actions/list-framework-documents.md) | `GET /frameworks/:frameworkId/documents` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [List Framework Projects](actions/list-framework-projects.md) | `GET /frameworks/:frameworkId/projects` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [List Framework Rules](actions/list-framework-rules.md) | `GET /frameworks/:frameworkId/rules` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [List Framework Section Rules](actions/list-framework-section-rules.md) | `GET /frameworks/:frameworkId/sections/:sectionId/rules` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [List Framework Subsection Rules](actions/list-framework-subsection-rules.md) | `GET /frameworks/:frameworkId/subsections/:subsectionId/rules` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [List Inference Pipeline Goals](actions/list-inference-pipeline-goals.md) | `GET /inference-pipelines/:inferencePipelineId/goals` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [List Inference Pipeline Results](actions/list-inference-pipeline-results.md) | `GET /inference-pipelines/:inferencePipelineId/results` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [List Inference Pipeline User Sessions](actions/list-inference-pipeline-user-sessions.md) | `GET /inference-pipelines/:inferencePipelineId/user/sessions` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [List Inference Pipelines](actions/list-inference-pipelines.md) | `GET /projects/:projectId/inference-pipelines` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [List Project Goals](actions/list-project-goals.md) | `GET /projects/:projectId/goals` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [List Project Metric Settings](actions/list-project-metric-settings.md) | `GET /projects/:projectId/metric-settings` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [List Project Tests](actions/list-project-tests.md) | `GET /projects/:projectId/tests` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [List Project User Tags](actions/list-project-user-tags.md) | `GET /projects/:projectId/user-tags` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [List Project Versions](actions/list-project-versions.md) | `GET /projects/:projectId/versions` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [List Rule Result Evidence](actions/list-rule-result-evidence.md) | `GET /rule-results/:ruleResultId/evidence` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [List Rule Result Goals](actions/list-rule-result-goals.md) | `GET /rule-results/:ruleResultId/goals` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [List Rule Results](actions/list-rule-results.md) | `GET /rules/:ruleId/results` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [List Version Goals](actions/list-version-goals.md) | `GET /versions/:versionId/goals` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [List Version Insights](actions/list-version-insights.md) | `POST /versions/:versionId/insights` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [List Version Results](actions/list-version-results.md) | `GET /versions/:versionId/results` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [List Workspace Frameworks](actions/list-workspace-frameworks.md) | `GET /workspaces/:workspaceId/frameworks` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [List Workspace Invites](actions/list-workspace-invites.md) | `GET /workspaces/:workspaceId/invites` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [List Workspace Rule Results](actions/list-workspace-rule-results.md) | `GET /workspaces/:workspaceId/rule-results` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [List Workspace Rule Tags](actions/list-workspace-rule-tags.md) | `GET /workspaces/:workspaceId/rule-tags` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [List Workspace Rules](actions/list-workspace-rules.md) | `GET /workspaces/:workspaceId/rules` | [docs](https://api.openlayer.com/v1/openapi.json) |
| [Update Project User Tag](actions/update-project-user-tag.md) | `PUT /projects/:projectId/user-tags/:tagId` | [docs](https://api.openlayer.com/v1/openapi.json) |
