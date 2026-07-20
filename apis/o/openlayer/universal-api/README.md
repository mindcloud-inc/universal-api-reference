# <img src="https://images.mindcloud.co/apps/icons/openlayer_1775734322833.png" alt="Openlayer logo" width="28" height="28"> Openlayer: Universal API

Openlayer API integration for workspace, project, monitoring, rules, and model-management workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/openlayer/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 51
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.openlayer.com
- **Vendor API docs:** https://api.openlayer.com/v1/openapi.json

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (51)

### Build Info

| Action | Method | Description |
| --- | --- | --- |
| [Get Build Info](actions/get-build-info.md) | GET | Retrieves build information from the Openlayer API. |

### Builds

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Version](actions/create-project-version.md) | POST | Creates a new project version in Openlayer. |
| [Export Version Data](actions/export-version-data.md) | POST | Exports version data from the Openlayer API. |
| [Get Project Version Upload URL](actions/get-project-version-upload-url.md) | GET | Retrieves a version upload URL for a project in Openlayer. |
| [Get Version](actions/get-version.md) | GET | Retrieves version details from the Openlayer API. |
| [List Version Goals](actions/list-version-goals.md) | GET | Retrieves goals for a version in Openlayer. |
| [List Version Insights](actions/list-version-insights.md) | GET | Retrieves insights for a version in Openlayer. |
| [List Version Results](actions/list-version-results.md) | GET | Retrieves results for a version in Openlayer. |

### Evidence

| Action | Method | Description |
| --- | --- | --- |
| [List Rule Result Evidence](actions/list-rule-result-evidence.md) | GET | Retrieves evidence for a rule result in Openlayer. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Create Storage Upload URL](actions/create-storage-upload-url.md) | POST | Creates a storage upload URL in Openlayer. |
| [Get Storage Download URL](actions/get-storage-download-url.md) | GET | Retrieves a storage download URL from Openlayer. |

### Framework

| Action | Method | Description |
| --- | --- | --- |
| [Get Framework](actions/get-framework.md) | GET | Retrieves framework details from the Openlayer API. |
| [List Workspace Frameworks](actions/list-workspace-frameworks.md) | GET | Retrieves frameworks for a workspace in Openlayer. |

### Framework Document

| Action | Method | Description |
| --- | --- | --- |
| [Get Framework Document](actions/get-framework-document.md) | GET | Retrieves a framework document from Openlayer. |
| [List Framework Documents](actions/list-framework-documents.md) | GET | Retrieves documents for a framework in Openlayer. |

### Framework Project

| Action | Method | Description |
| --- | --- | --- |
| [List Framework Projects](actions/list-framework-projects.md) | GET | Retrieves projects for a framework in Openlayer. |

### Goal

| Action | Method | Description |
| --- | --- | --- |
| [List Rule Result Goals](actions/list-rule-result-goals.md) | GET | Retrieves goals for a rule result in Openlayer. |

### Graph Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Inference Pipeline Graph Data](actions/get-inference-pipeline-graph-data.md) | GET | Retrieves graph data for an inference pipeline in Openlayer. |

### Health Check

| Action | Method | Description |
| --- | --- | --- |
| [Health Check](actions/health-check.md) | GET | Retrieves health check status from Openlayer. |

### Inference Pipeline

| Action | Method | Description |
| --- | --- | --- |
| [Create Inference Pipeline](actions/create-inference-pipeline.md) | POST | Creates a new inference pipeline in Openlayer. |
| [Get Inference Pipeline](actions/get-inference-pipeline.md) | GET | Retrieves an inference pipeline from Openlayer. |
| [List Inference Pipelines](actions/list-inference-pipelines.md) | GET | Retrieves inference pipelines for a project in Openlayer. |

### Inference Pipeline Goal

| Action | Method | Description |
| --- | --- | --- |
| [List Inference Pipeline Goals](actions/list-inference-pipeline-goals.md) | GET | Retrieves goals for an inference pipeline in Openlayer. |

### Inference Pipeline Result

| Action | Method | Description |
| --- | --- | --- |
| [List Inference Pipeline Results](actions/list-inference-pipeline-results.md) | GET | Retrieves results for an inference pipeline in Openlayer. |

### Metric Setting

| Action | Method | Description |
| --- | --- | --- |
| [List Project Metric Settings](actions/list-project-metric-settings.md) | GET | Retrieves metric settings for a project in Openlayer. |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile](actions/get-profile.md) | GET | Retrieves your profile details from Openlayer. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | GET | Retrieves a list of projects from Openlayer. |

### Project Test

| Action | Method | Description |
| --- | --- | --- |
| [List Project Tests](actions/list-project-tests.md) | GET | Retrieves tests for a project in Openlayer. |

### Project Version

| Action | Method | Description |
| --- | --- | --- |
| [List Project Versions](actions/list-project-versions.md) | GET | Retrieves versions for a project in Openlayer. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [List Project Goals](actions/list-project-goals.md) | GET | Retrieves goals for a project in Openlayer. |

### Rule

| Action | Method | Description |
| --- | --- | --- |
| [Get Rule](actions/get-rule.md) | GET | Retrieves rule details from the Openlayer API. |
| [List Framework Rules](actions/list-framework-rules.md) | GET | Retrieves rules for a framework in Openlayer. |
| [List Framework Section Rules](actions/list-framework-section-rules.md) | GET | Retrieves rules for a framework section in Openlayer. |
| [List Framework Subsection Rules](actions/list-framework-subsection-rules.md) | GET | Retrieves rules for a framework subsection in Openlayer. |
| [List Workspace Rules](actions/list-workspace-rules.md) | GET | Retrieves rules for a workspace in Openlayer. |

### Rule Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Rule Result](actions/get-rule-result.md) | GET | Retrieves a rule result from Openlayer. |
| [List Rule Results](actions/list-rule-results.md) | GET | Retrieves results for a rule in Openlayer. |
| [List Workspace Rule Results](actions/list-workspace-rule-results.md) | GET | Retrieves rule results for a workspace in Openlayer. |

### Rule Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Framework Project Rule Stats](actions/get-framework-project-rule-stats.md) | GET | Retrieves framework project rule statistics from Openlayer. |
| [Get Workspace Rule Stats](actions/get-workspace-rule-stats.md) | GET | Retrieves rule statistics for a workspace in Openlayer. |

### Rule Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Workspace Rule Tags](actions/list-workspace-rule-tags.md) | GET | Retrieves rule tags for a workspace in Openlayer. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create Project User Tag](actions/create-project-user-tag.md) | POST | Creates a new user tag for a project in Openlayer. |
| [Delete Project User Tag](actions/delete-project-user-tag.md) | DELETE | Deletes a project user tag from Openlayer. |
| [Update Project User Tag](actions/update-project-user-tag.md) | PUT | Updates an existing project user tag in Openlayer. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Inference Pipeline Session](actions/get-inference-pipeline-session.md) | GET | Retrieves a session for an inference pipeline in Openlayer. |
| [Get Inference Pipeline User](actions/get-inference-pipeline-user.md) | GET | Retrieves a user for an inference pipeline in Openlayer. |
| [List Inference Pipeline User Sessions](actions/list-inference-pipeline-user-sessions.md) | GET |  |

### User Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Project User Tags](actions/list-project-user-tags.md) | GET | Retrieves user tags for a project in Openlayer. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves workspace details from the Openlayer API. |

### Workspace Invite

| Action | Method | Description |
| --- | --- | --- |
| [List Workspace Invites](actions/list-workspace-invites.md) | GET | Retrieves invites for a workspace in Openlayer. |

### Workspace Public Key

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace Public Key](actions/get-workspace-public-key.md) | GET | Retrieves a workspace public key from Openlayer. |

