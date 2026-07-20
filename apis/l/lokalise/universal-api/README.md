# <img src="https://images.mindcloud.co/apps/icons/images-19_1774637949758.png" alt="Lokalise logo" width="28" height="28"> Lokalise: Universal API

Manage Lokalise translation projects, keys, files, and localization workflows from MindCloud.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lokalise/latest
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://lokalise.com
- **Vendor API docs:** https://developers.lokalise.com/reference/lokalise-rest-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Branch

| Action | Method | Description |
| --- | --- | --- |
| [List Branches](actions/list-branches.md) | GET | Retrieves branches from a Lokalise project. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Comments](actions/create-comments.md) | POST | Creates comments for a Lokalise key. |
| [Delete Comment](actions/delete-comment.md) | DELETE | Deletes a comment from a Lokalise key. |
| [List Key Comments](actions/list-key-comments.md) | GET | Retrieves comments for a Lokalise key. |

### Contributor

| Action | Method | Description |
| --- | --- | --- |
| [Create Contributors](actions/create-contributors.md) | POST | Creates contributors in a Lokalise project. |
| [Delete Contributor](actions/delete-contributor.md) | DELETE | Deletes an existing contributor from Lokalise. |
| [List Contributors](actions/list-contributors.md) | GET | Retrieves contributors from a Lokalise project. |
| [Update Contributor](actions/update-contributor.md) | PUT | Updates an existing contributor in Lokalise. |

### Key

| Action | Method | Description |
| --- | --- | --- |
| [Create Keys](actions/create-keys.md) | POST | Creates keys in a Lokalise project. |
| [Delete Key](actions/delete-key.md) | DELETE | Deletes an existing key from Lokalise. |
| [List Keys](actions/list-keys.md) | GET | Retrieves keys from a Lokalise project. |
| [Retrieve Key](actions/retrieve-key.md) | GET | Retrieves a key from a Lokalise project. |
| [Update Key](actions/update-key.md) | PUT | Updates an existing key in Lokalise. |

### Language

| Action | Method | Description |
| --- | --- | --- |
| [List Project Languages](actions/list-project-languages.md) | GET | Retrieves project languages from Lokalise. |

### Process

| Action | Method | Description |
| --- | --- | --- |
| [Download Files Async](actions/download-files-async.md) | POST | Starts an asynchronous file download in Lokalise. |
| [List Processes](actions/list-processes.md) | GET | Retrieves processes from a Lokalise project. |
| [Retrieve Process](actions/retrieve-process.md) | GET | Retrieves a process from a Lokalise project. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Lokalise. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Lokalise. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Lokalise. |
| [Retrieve Project](actions/retrieve-project.md) | GET | Retrieves a project from Lokalise. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Lokalise. |

### Screenshot

| Action | Method | Description |
| --- | --- | --- |
| [Create Screenshots](actions/create-screenshots.md) | POST | Creates screenshots in a Lokalise project. |
| [Delete Screenshot](actions/delete-screenshot.md) | DELETE | Deletes a screenshot from a Lokalise project. |
| [List Screenshots](actions/list-screenshots.md) | GET | Retrieves screenshots from a Lokalise project. |
| [Retrieve Screenshot](actions/retrieve-screenshot.md) | GET | Retrieves a screenshot from a Lokalise project. |

### Snapshot

| Action | Method | Description |
| --- | --- | --- |
| [Create Snapshot](actions/create-snapshot.md) | POST | Creates a snapshot in a Lokalise project. |
| [Delete Snapshot](actions/delete-snapshot.md) | DELETE | Deletes a snapshot from a Lokalise project. |
| [List Snapshots](actions/list-snapshots.md) | GET | Retrieves snapshots from a Lokalise project. |
| [Restore Snapshot](actions/restore-snapshot.md) | POST | Restores a snapshot in a Lokalise project. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from a Lokalise project. |

### Translation

| Action | Method | Description |
| --- | --- | --- |
| [List Translations](actions/list-translations.md) | GET | Retrieves translations from a Lokalise project. |

