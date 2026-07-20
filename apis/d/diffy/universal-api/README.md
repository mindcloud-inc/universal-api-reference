# <img src="https://images.mindcloud.co/apps/icons/diffy-idr-ulo-x-im-0_1775494917282.png" alt="Diffy logo" width="28" height="28"> Diffy: Universal API

Create visual tests, compare screenshots, and review diffs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/diffy/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://diffy.website
- **Vendor API docs:** https://app.diffy.website/rest

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diffy/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Uploaded Screenshot](actions/create-custom-uploaded-screenshot.md) | POST | Creates a custom uploaded screenshot in Diffy. |
| [Create Screenshot](actions/create-screenshot.md) | POST | Creates a project screenshot in Diffy. |
| [Delete Screenshot](actions/delete-screenshot.md) | DELETE | Deletes an existing screenshot from Diffy. |
| [Get Screenshot](actions/get-screenshot.md) | GET | Retrieves a single screenshot from Diffy. |
| [List Project Screenshots](actions/list-project-screenshots.md) | GET | Retrieves screenshots for a project from Diffy. |
| [Set Baseline Image](actions/set-baseline-image.md) | PUT | Sets a baseline image in Diffy. |
| [Set Screenshot Set as Baseline](actions/set-screenshot-set-as-baseline.md) | PUT | Sets a screenshot set as baseline in Diffy. |
| [Start or Stop Screenshot Jobs](actions/start-or-stop-screenshot-jobs.md) | PUT | Starts or stops screenshot jobs in Diffy. |
| [Update Screenshot](actions/update-screenshot.md) | PUT | Updates a screenshot name in Diffy. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Diffy. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Diffy. |
| [Get Project](actions/get-project.md) | GET | Retrieves a single project from Diffy. |
| [List Projects](actions/list-projects.md) | GET | Retrieves the project list from Diffy. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Diffy. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Compare Environments](actions/compare-environments.md) | POST | Creates an environment comparison diff in Diffy. |
| [Create Diff](actions/create-diff.md) | POST | Creates a screenshot diff in Diffy. |
| [Delete Diff](actions/delete-diff.md) | DELETE | Deletes an existing diff from Diffy. |
| [Get Diff](actions/get-diff.md) | GET | Retrieves a single diff from Diffy. |
| [List Project Diffs](actions/list-project-diffs.md) | GET | Retrieves diffs for a project from Diffy. |
| [Start or Stop Diff Jobs](actions/start-or-stop-diff-jobs.md) | PUT | Starts or stops diff jobs in Diffy. |
| [Update Diff Name](actions/update-diff-name.md) | PUT | Updates a diff name in Diffy. |

### Token

| Action | Method | Description |
| --- | --- | --- |
| [Exchange API Key for Token](actions/exchange-api-key-for-token.md) | POST | Creates an access token in Diffy. |

