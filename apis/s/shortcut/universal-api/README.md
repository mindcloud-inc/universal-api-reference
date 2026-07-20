# <img src="https://images.mindcloud.co/apps/icons/shortcut_1773760808855.png" alt="Shortcut logo" width="28" height="28"> Shortcut: Universal API

Manage stories, epics, projects, and workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/shortcut/latest
- **Category:** Support / Ticketing
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://shortcut.com
- **Vendor API docs:** https://developer.shortcut.com/api/rest/v3

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [List Epic Comments](actions/list-epic-comments.md) | GET |  |
| [List Story Comments](actions/list-story-comments.md) | GET |  |

### Epic

| Action | Method | Description |
| --- | --- | --- |
| [Create Epic](actions/create-epic.md) | POST |  |
| [Get Epic](actions/get-epic.md) | GET |  |
| [List Epics](actions/list-epics.md) | GET |  |
| [List Milestone Epics](actions/list-milestone-epics.md) | GET |  |
| [List Objective Epics](actions/list-objective-epics.md) | GET |  |
| [Update Epic](actions/update-epic.md) | PUT |  |

### Epic Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Epic Comment](actions/create-epic-comment.md) | POST |  |
| [Update Epic Comment](actions/update-epic-comment.md) | PUT |  |

### Iteration

| Action | Method | Description |
| --- | --- | --- |
| [Create Iteration](actions/create-iteration.md) | POST |  |
| [Get Iteration](actions/get-iteration.md) | GET |  |
| [List Iterations](actions/list-iterations.md) | GET |  |
| [Update Iteration](actions/update-iteration.md) | PUT |  |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Member Info](actions/get-current-member-info.md) | GET |  |
| [Get Member](actions/get-member.md) | GET |  |
| [List Members](actions/list-members.md) | GET |  |

### Milestone

| Action | Method | Description |
| --- | --- | --- |
| [Create Milestone](actions/create-milestone.md) | POST |  |
| [Get Milestone](actions/get-milestone.md) | GET |  |
| [List Milestones](actions/list-milestones.md) | GET |  |
| [Update Milestone](actions/update-milestone.md) | PUT |  |

### Objective

| Action | Method | Description |
| --- | --- | --- |
| [Create Objective](actions/create-objective.md) | POST |  |
| [Get Objective](actions/get-objective.md) | GET |  |
| [List Objectives](actions/list-objectives.md) | GET |  |
| [Update Objective](actions/update-objective.md) | PUT |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST |  |
| [Get Project](actions/get-project.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |
| [Update Project](actions/update-project.md) | PUT |  |

### Story

| Action | Method | Description |
| --- | --- | --- |
| [Create Story](actions/create-story.md) | POST |  |
| [Get Story](actions/get-story.md) | GET |  |
| [List Epic Stories](actions/list-epic-stories.md) | GET |  |
| [List Iteration Stories](actions/list-iteration-stories.md) | GET |  |
| [List Project Stories](actions/list-project-stories.md) | GET |  |
| [Search Stories](actions/search-stories.md) | GET |  |
| [Update Story](actions/update-story.md) | PUT |  |

### Story Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Story Comment](actions/create-story-comment.md) | POST |  |
| [Update Story Comment](actions/update-story-comment.md) | PUT |  |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow](actions/get-workflow.md) | GET |  |
| [List Workflows](actions/list-workflows.md) | GET |  |

