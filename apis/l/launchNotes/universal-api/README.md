# <img src="https://images.mindcloud.co/apps/icons/launch-notes_1775054514431.png" alt="LaunchNotes logo" width="28" height="28"> LaunchNotes: Universal API

Manage announcements, feedback, ideas, stages, and work items in LaunchNotes.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/launchNotes/latest
- **Category:** Productivity / Project Management
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.launchnotes.com
- **Vendor API docs:** https://developer.launchnotes.com/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Viewer](actions/get-viewer.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/get-viewer?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Announcement Digest

| Action | Method | Description |
| --- | --- | --- |
| [Get Announcement Digest](actions/get-announcement-digest.md) | GET |  |

### Announcements

| Action | Method | Description |
| --- | --- | --- |
| [Archive Announcement](actions/archive-announcement.md) | PUT |  |
| [Copy Announcement To Project](actions/copy-announcement-to-project.md) | POST |  |
| [Create AI Announcement](actions/create-ai-announcement.md) | POST |  |
| [Create Announcement](actions/create-announcement.md) | POST |  |
| [Duplicate Announcement](actions/duplicate-announcement.md) | POST |  |
| [Get Announcement](actions/get-announcement.md) | GET |  |
| [Publish Announcement](actions/publish-announcement.md) | PUT |  |
| [Schedule Announcement](actions/schedule-announcement.md) | PUT |  |
| [Unarchive Announcement](actions/unarchive-announcement.md) | PUT |  |
| [Unpublish Announcement](actions/unpublish-announcement.md) | PUT |  |
| [Unschedule Announcement](actions/unschedule-announcement.md) | PUT |  |
| [Update Announcement](actions/update-announcement.md) | PUT |  |

### Feedback

| Action | Method | Description |
| --- | --- | --- |
| [Archive Feedback](actions/archive-feedback.md) | PUT |  |
| [Create Feedback](actions/create-feedback.md) | POST |  |
| [Get Feedback](actions/get-feedback.md) | GET |  |
| [Unarchive Feedback](actions/unarchive-feedback.md) | PUT |  |
| [Update Feedback](actions/update-feedback.md) | PUT |  |

### Feedback Import

| Action | Method | Description |
| --- | --- | --- |
| [Import Feedback](actions/import-feedback.md) | POST |  |

### Idea

| Action | Method | Description |
| --- | --- | --- |
| [Archive Ideas](actions/archive-ideas.md) | PUT |  |
| [Create Idea](actions/create-idea.md) | POST |  |
| [Get Idea](actions/get-idea.md) | GET |  |
| [Toggle Published Idea](actions/toggle-published-idea.md) | PUT |  |
| [Unarchive Ideas](actions/unarchive-ideas.md) | PUT |  |
| [Update Idea](actions/update-idea.md) | PUT |  |

### Node

| Action | Method | Description |
| --- | --- | --- |
| [Get Node](actions/get-node.md) | GET |  |
| [List Nodes](actions/list-nodes.md) | GET |  |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET |  |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Project](actions/search-project.md) | GET |  |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Get Session](actions/get-session.md) | GET |  |

### Stages

| Action | Method | Description |
| --- | --- | --- |
| [Create Stage](actions/create-stage.md) | POST |  |
| [Update Stage](actions/update-stage.md) | PUT |  |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Viewer](actions/get-viewer.md) | GET |  |

### Work Item

| Action | Method | Description |
| --- | --- | --- |
| [Archive Work Item](actions/archive-work-item.md) | PUT |  |
| [Create Work Item](actions/create-work-item.md) | POST |  |
| [Get Work Item](actions/get-work-item.md) | GET |  |
| [Promote Idea](actions/promote-idea.md) | POST |  |
| [Publish Work Item](actions/publish-work-item.md) | PUT |  |
| [Update Work Item](actions/update-work-item.md) | PUT |  |

