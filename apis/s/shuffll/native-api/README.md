# Shuffll: Native API Reference

A consolidated summary of Shuffll's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://api-docs.shuffll.com/apis
- **OpenAPI specification:** https://api-docs.shuffll.com/_bundle/apis/index.json?download=
- **API base URL:** `https://api.shuffll.com/api/v1`

## Authentication

### API Key

Use your Shuffll API key. Shuffll authenticates every request through the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://api-docs.shuffll.com/apis/enhance)

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Asset Folder](actions/create-asset-folder.md) | `POST /auth/organization/:organizationId/workspace/:workspaceId/assets/folder` | [docs](https://api-docs.shuffll.com/apis/assets/createassetfolder) |
| [Create Project](actions/create-project.md) | `POST /auth/project/create` | [docs](https://api-docs.shuffll.com/apis/projects/createproject) |
| [Delete Assets](actions/delete-assets.md) | `DELETE /auth/organization/:organizationId/workspace/:workspaceId/assets` | [docs](https://api-docs.shuffll.com/apis/assets/deleteassets) |
| [Delete Project](actions/delete-project.md) | `DELETE /auth/project/:projectId` | [docs](https://api-docs.shuffll.com/apis/projects/deleteproject) |
| [Export Project](actions/export-project.md) | `POST /auth/project/:projectId/edit/export` | [docs](https://api-docs.shuffll.com/apis/export/exportproject) |
| [Get Organization](actions/get-organization.md) | `GET /auth/organization/:organizationId` | [docs](https://api-docs.shuffll.com/apis/organizations/getorganizationbyid) |
| [Get Project](actions/get-project.md) | `GET /auth/project/:projectId` | [docs](https://api-docs.shuffll.com/apis/projects/getprojectbyid) |
| [Get Project Creation Status](actions/get-project-creation-status.md) | `GET /auth/project/:projectId/create/status` | [docs](https://api-docs.shuffll.com/apis/projects/getprojectcreatestatus) |
| [Get Project Enhancement Status](actions/get-project-enhancement-status.md) | `GET /auth/project/:projectId/edit/status/enhance` | [docs](https://api-docs.shuffll.com/apis/enhance/getenhancestatus) |
| [Get Project Export Status](actions/get-project-export-status.md) | `GET /auth/project/:projectId/edit/status/export` | [docs](https://api-docs.shuffll.com/apis/export/getexportstatus) |
| [Get Workspace](actions/get-workspace.md) | `GET /auth/organization/:organizationId/workspace/:workspaceId` | [docs](https://api-docs.shuffll.com/apis/workspaces/getworkspacebyid) |
| [List AI Avatar Options](actions/list-ai-avatar-options.md) | `GET /auth/config/ai_avatar_options` | [docs](https://api-docs.shuffll.com/apis/configuration/getaiavataroptions) |
| [List AI Voice Options](actions/list-ai-voice-options.md) | `GET /auth/config/ai_voice_options` | [docs](https://api-docs.shuffll.com/apis/configuration/getaivoiceoptions) |
| [List Assets](actions/list-assets.md) | `GET /auth/organization/:organizationId/workspace/:workspaceId/assets` | [docs](https://api-docs.shuffll.com/apis/assets/listassets) |
| [List Music Library](actions/list-music-library.md) | `GET /auth/config/music-library` | [docs](https://api-docs.shuffll.com/apis/configuration/getmusiclibrary) |
| [List Organizations](actions/list-organizations.md) | `GET /auth/organization/list` | [docs](https://api-docs.shuffll.com/apis/organizations/getorganizationlist) |
| [List Storytelling Techniques](actions/list-storytelling-techniques.md) | `GET /auth/config/storytelling_techniques` | [docs](https://api-docs.shuffll.com/apis/configuration/getstorytellingtechniques) |
| [List Templates](actions/list-templates.md) | `GET /auth/templates` | [docs](https://api-docs.shuffll.com/apis/templates/getalltemplates) |
| [List Tone of Voice Options](actions/list-tone-of-voice-options.md) | `GET /auth/config/tone_of_voice` | [docs](https://api-docs.shuffll.com/apis/configuration/gettoneofvoice) |
| [List Video Tags](actions/list-video-tags.md) | `GET /auth/config/video_tags` | [docs](https://api-docs.shuffll.com/apis/configuration/getvideotags) |
| [List Workspace Templates](actions/list-workspace-templates.md) | `GET /auth/organization/:organizationId/workspace/:workspaceId/templates` | [docs](https://api-docs.shuffll.com/apis/templates/gettemplatesbyorgworkspace) |
| [Move Assets](actions/move-assets.md) | `PUT /auth/organization/:organizationId/workspace/:workspaceId/assets/move` | [docs](https://api-docs.shuffll.com/apis/assets/moveassets) |
| [Rename Asset](actions/rename-asset.md) | `PUT /auth/organization/:organizationId/workspace/:workspaceId/assets/:assetId/file` | [docs](https://api-docs.shuffll.com/apis/assets/renameasset) |
| [Set Branding Enabled](actions/set-branding-enabled.md) | `PUT /auth/branding/entity` | [docs](https://api-docs.shuffll.com/apis/branding/updatebranding) |
| [Update Workspace](actions/update-workspace.md) | `PUT /auth/organization/:organizationId/workspace/:workspaceId` | [docs](https://api-docs.shuffll.com/apis/workspaces/updateworkspace) |
