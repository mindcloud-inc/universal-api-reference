# <img src="https://images.mindcloud.co/apps/icons/img-0547594574-150x150_1774977949895.png" alt="Shuffll logo" width="28" height="28"> Shuffll: Universal API

API wrapper for Shuffll's AI-powered video creation platform, covering configuration catalogs, organizations, workspaces, branding, assets, templates, projects, enhancement status, and export workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/shuffll/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://shuffll.com
- **Vendor API docs:** https://api-docs.shuffll.com/apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organizations](actions/list-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Ai Avatar Option

| Action | Method | Description |
| --- | --- | --- |
| [List AI Avatar Options](actions/list-ai-avatar-options.md) | GET | Retrieves AI avatar options from Shuffll. |

### Ai Voice Option

| Action | Method | Description |
| --- | --- | --- |
| [List AI Voice Options](actions/list-ai-voice-options.md) | GET | Retrieves AI voice options from Shuffll. |

### Asset

| Action | Method | Description |
| --- | --- | --- |
| [Delete Assets](actions/delete-assets.md) | DELETE | Deletes existing assets from Shuffll. |
| [List Assets](actions/list-assets.md) | GET | Retrieves assets from Shuffll. |
| [Move Assets](actions/move-assets.md) | PUT | Updates asset locations in Shuffll. |
| [Rename Asset](actions/rename-asset.md) | PUT | Updates an asset name in Shuffll. |

### Asset Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Asset Folder](actions/create-asset-folder.md) | POST | Creates a new asset folder in Shuffll. |

### Branding

| Action | Method | Description |
| --- | --- | --- |
| [Set Branding Enabled](actions/set-branding-enabled.md) | PUT | Updates branding settings in Shuffll. |

### Music Track

| Action | Method | Description |
| --- | --- | --- |
| [List Music Library](actions/list-music-library.md) | GET | Retrieves music library items from Shuffll. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from Shuffll by ID. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from Shuffll. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Shuffll. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Shuffll. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Shuffll by ID. |

### Project Creation Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Creation Status](actions/get-project-creation-status.md) | GET | Retrieves project creation status from Shuffll. |

### Project Enhancement Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Enhancement Status](actions/get-project-enhancement-status.md) | GET | Retrieves project enhancement status from Shuffll. |

### Project Export

| Action | Method | Description |
| --- | --- | --- |
| [Export Project](actions/export-project.md) | POST | Creates a project export in Shuffll. |

### Project Export Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Export Status](actions/get-project-export-status.md) | GET | Retrieves project export status from Shuffll. |

### Storytelling Technique

| Action | Method | Description |
| --- | --- | --- |
| [List Storytelling Techniques](actions/list-storytelling-techniques.md) | GET | Retrieves storytelling techniques from Shuffll. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from Shuffll. |
| [List Workspace Templates](actions/list-workspace-templates.md) | GET | Retrieves workspace templates from Shuffll. |

### Tone Of Voice

| Action | Method | Description |
| --- | --- | --- |
| [List Tone of Voice Options](actions/list-tone-of-voice-options.md) | GET | Retrieves tone of voice options from Shuffll. |

### Video Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Video Tags](actions/list-video-tags.md) | GET | Retrieves video tags from Shuffll. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves a workspace from Shuffll by ID. |
| [Update Workspace](actions/update-workspace.md) | PUT | Updates an existing workspace in Shuffll. |

