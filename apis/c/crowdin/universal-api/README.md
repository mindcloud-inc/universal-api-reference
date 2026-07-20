# <img src="https://images.mindcloud.co/apps/icons/crowdin_1774390158875.png" alt="Crowdin logo" width="28" height="28"> Crowdin: Universal API

Crowdin: Localize software, apps, websites, and content

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/crowdin/latest
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://crowdin.com
- **Vendor API docs:** https://support.crowdin.com/developer/api/v2/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authenticated User](actions/get-authenticated-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Branch

| Action | Method | Description |
| --- | --- | --- |
| [Add Branch](actions/add-branch.md) | POST | Creates a new branch in a Crowdin project. |
| [List Branches](actions/list-branches.md) | GET | Retrieves branches from a Crowdin project. |

### Builds

| Action | Method | Description |
| --- | --- | --- |
| [Build Project Translation](actions/build-project-translation.md) | POST | Starts a project translation build in Crowdin. |
| [Get Project Build Status](actions/get-project-build-status.md) | GET | Retrieves project build status from Crowdin. |
| [List Project Builds](actions/list-project-builds.md) | GET | Retrieves project builds from Crowdin. |

### Download Link

| Action | Method | Description |
| --- | --- | --- |
| [Download File](actions/download-file.md) | GET | Retrieves a download link for a file in Crowdin. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Add File](actions/add-file.md) | POST | Creates a new file in a Crowdin project. |
| [Edit File](actions/edit-file.md) | PUT | Updates an existing file in a Crowdin project. |
| [Get File](actions/get-file.md) | GET | Retrieves a file from a Crowdin project. |
| [List Files](actions/list-files.md) | GET | Retrieves files from a Crowdin project. |

### File Versions

| Action | Method | Description |
| --- | --- | --- |
| [List File Revisions](actions/list-file-revisions.md) | GET | Retrieves file revisions from a Crowdin project. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Add Storage](actions/add-storage.md) | POST | Uploads a file to Crowdin storage. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Add Directory](actions/add-directory.md) | POST | Creates a new directory in a Crowdin project. |
| [List Directories](actions/list-directories.md) | GET | Retrieves directories from a Crowdin project. |

### Language

| Action | Method | Description |
| --- | --- | --- |
| [List Supported Languages](actions/list-supported-languages.md) | GET | Retrieves supported languages from Crowdin. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Add Project](actions/add-project.md) | POST | Creates a new project in Crowdin. |
| [Edit Project](actions/edit-project.md) | PUT | Updates an existing project in Crowdin. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Crowdin. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Crowdin. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Add Project Task](actions/add-project-task.md) | POST | Creates a new project task in Crowdin. |
| [Get Project Task](actions/get-project-task.md) | GET | Retrieves a project task from Crowdin. |
| [List Project Tasks](actions/list-project-tasks.md) | GET | Retrieves project tasks from Crowdin. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Download Project Translations](actions/download-project-translations.md) | GET | Retrieves a download link for project translations in Crowdin. |
| [Get Project Progress](actions/get-project-progress.md) | GET | Retrieves project progress by language from Crowdin. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Authenticated User](actions/get-authenticated-user.md) | GET | Retrieves the authenticated user from Crowdin. |

