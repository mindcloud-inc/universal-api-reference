# <img src="https://images.mindcloud.co/apps/icons/e2b_1776099305565.png" alt="E2B logo" width="28" height="28"> E2B: Universal API

E2B provides secure cloud sandboxes, templates, volumes, and team metrics for AI agent and developer automation workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/e2B/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 37
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://e2b.dev
- **Vendor API docs:** https://e2b.dev/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sandboxes](actions/list-sandboxes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/e2B/latest/actions/list-sandboxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (37)

### Sandbox

| Action | Method | Description |
| --- | --- | --- |
| [Connect To Sandbox](actions/connect-to-sandbox.md) | GET | Retrieves sandbox details from E2B and resumes it if paused. |
| [Create Sandbox](actions/create-sandbox.md) | POST | Creates a sandbox from a template in E2B. |
| [Delete Sandbox](actions/delete-sandbox.md) | DELETE | Deletes a sandbox from E2B. |
| [Get Sandbox](actions/get-sandbox.md) | GET | Retrieves details for a sandbox from E2B. |
| [List Sandboxes](actions/list-sandboxes.md) | GET | Retrieves a list of running sandboxes from E2B. |
| [List Sandboxes V2](actions/list-sandboxes-v2.md) | GET | Retrieves a list of sandboxes from E2B. |
| [Pause Sandbox](actions/pause-sandbox.md) | PUT | Pauses a sandbox in E2B. |
| [Refresh Sandbox](actions/refresh-sandbox.md) | PUT | Refreshes a sandbox in E2B, extending its time to live. |
| [Resume Sandbox](actions/resume-sandbox.md) | PUT | Resumes a sandbox in E2B. |
| [Set Sandbox Timeout](actions/set-sandbox-timeout.md) | PUT | Sets a sandbox timeout in E2B. |

### Sandbox Log

| Action | Method | Description |
| --- | --- | --- |
| [Get Sandbox Logs V2](actions/get-sandbox-logs-v2.md) | GET | Retrieves logs for a sandbox from E2B. |

### Sandbox Metric

| Action | Method | Description |
| --- | --- | --- |
| [Get Sandbox Metrics](actions/get-sandbox-metrics.md) | GET | Retrieves metrics for a sandbox from E2B. |
| [List Sandbox Metrics](actions/list-sandbox-metrics.md) | GET | Retrieves metrics for sandboxes from E2B. |

### Sandbox Network

| Action | Method | Description |
| --- | --- | --- |
| [Update Sandbox Network](actions/update-sandbox-network.md) | PUT | Updates sandbox network settings in E2B. |

### Snapshot

| Action | Method | Description |
| --- | --- | --- |
| [Create Sandbox Snapshot](actions/create-sandbox-snapshot.md) | POST | Creates a snapshot from a sandbox in E2B. |
| [List Snapshots](actions/list-snapshots.md) | GET | Retrieves a list of snapshots from E2B. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a new template in E2B. |
| [Create Template V3](actions/create-template-v3.md) | POST | Creates a new template in E2B. |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes a template from E2B. |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from E2B. |
| [Get Template By Alias](actions/get-template-by-alias.md) | GET | Finds a template in E2B by alias. |
| [List Templates](actions/list-templates.md) | GET | Retrieves a list of templates from E2B. |
| [Rebuild Template](actions/rebuild-template.md) | PUT | Rebuilds a template in E2B. |
| [Update Template](actions/update-template.md) | PUT | Updates an existing template in E2B. |
| [Update Template V2](actions/update-template-v2.md) | PUT | Updates an existing template in E2B. |

### Template Build

| Action | Method | Description |
| --- | --- | --- |
| [Get Build Status](actions/get-build-status.md) | GET | Retrieves template build status from E2B. |
| [Start Build](actions/start-build.md) | PUT | Starts a template build in E2B. |
| [Start Build V2](actions/start-build-v2.md) | PUT | Starts a template build in E2B. |

### Template Build Log

| Action | Method | Description |
| --- | --- | --- |
| [Get Build Logs](actions/get-build-logs.md) | GET | Retrieves logs for a template build from E2B. |

### Template Build Upload

| Action | Method | Description |
| --- | --- | --- |
| [Get Build Upload Link](actions/get-build-upload-link.md) | GET | Retrieves a build upload link from E2B. |

### Template Tag

| Action | Method | Description |
| --- | --- | --- |
| [Assign Tags](actions/assign-tags.md) | POST | Assigns tags to a template build in E2B. |
| [Delete Tags](actions/delete-tags.md) | DELETE | Deletes tags from templates in E2B. |
| [List Template Tags](actions/list-template-tags.md) | GET | Retrieves a list of template tags from E2B. |

### Volume

| Action | Method | Description |
| --- | --- | --- |
| [Create Volume](actions/create-volume.md) | POST | Creates a new team volume in E2B. |
| [Delete Volume](actions/delete-volume.md) | DELETE | Deletes a team volume from E2B. |
| [Get Volume](actions/get-volume.md) | GET | Retrieves a team volume from E2B. |
| [List Volumes](actions/list-volumes.md) | GET | Retrieves a list of team volumes from E2B. |

