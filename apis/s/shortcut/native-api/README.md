# Shortcut: Native API Reference

A consolidated summary of Shortcut's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developer.shortcut.com/api/rest/v3
- **OpenAPI specification:** https://developer.shortcut.com/api/rest/v3/shortcut.openapi.json
- **API base URL:** `https://api.app.shortcut.com/api/v3`

## Authentication

### API Key

Use a Shortcut API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.shortcut.com/hc/en-us/articles/205701199-Shortcut-API-Tokens)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `next`.

## Pagination

Use `page_size` in the query string to set the page size. Use `next` in the query string as the pagination cursor.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Epic](actions/create-epic.md) | `POST /epics` | [docs](https://developer.shortcut.com/api/rest/v3#Create-Epic) |
| [Create Epic Comment](actions/create-epic-comment.md) | `POST /epics/:epicPublicId/comments` | [docs](https://developer.shortcut.com/api/rest/v3#Create-Epic-Comment) |
| [Create Iteration](actions/create-iteration.md) | `POST /iterations` | [docs](https://developer.shortcut.com/api/rest/v3#Create-Iteration) |
| [Create Milestone](actions/create-milestone.md) | `POST /milestones` | [docs](https://developer.shortcut.com/api/rest/v3#Create-Milestone) |
| [Create Objective](actions/create-objective.md) | `POST /objectives` | [docs](https://developer.shortcut.com/api/rest/v3#Create-Objective) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://developer.shortcut.com/api/rest/v3#Create-Project) |
| [Create Story](actions/create-story.md) | `POST /stories` | [docs](https://developer.shortcut.com/api/rest/v3#Create-Story) |
| [Create Story Comment](actions/create-story-comment.md) | `POST /stories/:storyPublicId/comments` | [docs](https://developer.shortcut.com/api/rest/v3#Create-Story-Comment) |
| [Get Current Member Info](actions/get-current-member-info.md) | `GET /member` | [docs](https://developer.shortcut.com/api/rest/v3#Get-Current-Member-Info) |
| [Get Epic](actions/get-epic.md) | `GET /epics/:epicPublicId` | [docs](https://developer.shortcut.com/api/rest/v3#Get-Epic) |
| [Get Iteration](actions/get-iteration.md) | `GET /iterations/:iterationPublicId` | [docs](https://developer.shortcut.com/api/rest/v3#Get-Iteration) |
| [Get Member](actions/get-member.md) | `GET /members/:memberPublicId` | [docs](https://developer.shortcut.com/api/rest/v3#Get-Member) |
| [Get Milestone](actions/get-milestone.md) | `GET /milestones/:milestonePublicId` | [docs](https://developer.shortcut.com/api/rest/v3#Get-Milestone) |
| [Get Objective](actions/get-objective.md) | `GET /objectives/:objectivePublicId` | [docs](https://developer.shortcut.com/api/rest/v3#Get-Objective) |
| [Get Project](actions/get-project.md) | `GET /projects/:projectPublicId` | [docs](https://developer.shortcut.com/api/rest/v3#Get-Project) |
| [Get Story](actions/get-story.md) | `GET /stories/:storyPublicId` | [docs](https://developer.shortcut.com/api/rest/v3#Get-Story) |
| [Get Workflow](actions/get-workflow.md) | `GET /workflows/:workflowPublicId` | [docs](https://developer.shortcut.com/api/rest/v3#Get-Workflow) |
| [List Epic Comments](actions/list-epic-comments.md) | `GET /epics/:epicPublicId/comments` | [docs](https://developer.shortcut.com/api/rest/v3#List-Epic-Comments) |
| [List Epic Stories](actions/list-epic-stories.md) | `GET /epics/:epicPublicId/stories` | [docs](https://developer.shortcut.com/api/rest/v3#List-Epic-Stories) |
| [List Epics](actions/list-epics.md) | `GET /epics` | [docs](https://developer.shortcut.com/api/rest/v3#List-Epics) |
| [List Iteration Stories](actions/list-iteration-stories.md) | `GET /iterations/:iterationPublicId/stories` | [docs](https://developer.shortcut.com/api/rest/v3#List-Iteration-Stories) |
| [List Iterations](actions/list-iterations.md) | `GET /iterations` | [docs](https://developer.shortcut.com/api/rest/v3#List-Iterations) |
| [List Members](actions/list-members.md) | `GET /members` | [docs](https://developer.shortcut.com/api/rest/v3#List-Members) |
| [List Milestone Epics](actions/list-milestone-epics.md) | `GET /milestones/:milestonePublicId/epics` | [docs](https://developer.shortcut.com/api/rest/v3#List-Milestone-Epics) |
| [List Milestones](actions/list-milestones.md) | `GET /milestones` | [docs](https://developer.shortcut.com/api/rest/v3#List-Milestones) |
| [List Objective Epics](actions/list-objective-epics.md) | `GET /objectives/:objectivePublicId/epics` | [docs](https://developer.shortcut.com/api/rest/v3#List-Objective-Epics) |
| [List Objectives](actions/list-objectives.md) | `GET /objectives` | [docs](https://developer.shortcut.com/api/rest/v3#List-Objectives) |
| [List Project Stories](actions/list-project-stories.md) | `GET /projects/:projectPublicId/stories` | [docs](https://developer.shortcut.com/api/rest/v3#List-Stories) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://developer.shortcut.com/api/rest/v3#List-Projects) |
| [List Story Comments](actions/list-story-comments.md) | `GET /stories/:storyPublicId/comments` | [docs](https://developer.shortcut.com/api/rest/v3#List-Story-Comment) |
| [List Workflows](actions/list-workflows.md) | `GET /workflows` | [docs](https://developer.shortcut.com/api/rest/v3#List-Workflows) |
| [Search Stories](actions/search-stories.md) | `GET /search/stories` | [docs](https://developer.shortcut.com/api/rest/v3#Search-Stories) |
| [Update Epic](actions/update-epic.md) | `PUT /epics/:epicPublicId` | [docs](https://developer.shortcut.com/api/rest/v3#Update-Epic) |
| [Update Epic Comment](actions/update-epic-comment.md) | `PUT /epics/:epicPublicId/comments/:commentPublicId` | [docs](https://developer.shortcut.com/api/rest/v3#Update-Epic-Comment) |
| [Update Iteration](actions/update-iteration.md) | `PUT /iterations/:iterationPublicId` | [docs](https://developer.shortcut.com/api/rest/v3#Update-Iteration) |
| [Update Milestone](actions/update-milestone.md) | `PUT /milestones/:milestonePublicId` | [docs](https://developer.shortcut.com/api/rest/v3#Update-Milestone) |
| [Update Objective](actions/update-objective.md) | `PUT /objectives/:objectivePublicId` | [docs](https://developer.shortcut.com/api/rest/v3#Update-Objective) |
| [Update Project](actions/update-project.md) | `PUT /projects/:projectPublicId` | [docs](https://developer.shortcut.com/api/rest/v3#Update-Project) |
| [Update Story](actions/update-story.md) | `PUT /stories/:storyPublicId` | [docs](https://developer.shortcut.com/api/rest/v3#Update-Story) |
| [Update Story Comment](actions/update-story-comment.md) | `PUT /stories/:storyPublicId/comments/:storyCommentPublicId` | [docs](https://developer.shortcut.com/api/rest/v3#Update-Story-Comment) |
