# <img src="https://images.mindcloud.co/apps/icons/id-pd-8vrqt-logos_1773941902961.png" alt="Userback logo" width="28" height="28"> Userback: Universal API

Userback is a product feedback and bug reporting platform for collecting, managing, and acting on customer feedback.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/userback/latest
- **Category:** Support / Customer Success
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://userback.io
- **Vendor API docs:** https://docs.userback.io/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userback/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Feedback

| Action | Method | Description |
| --- | --- | --- |
| [Create Feedback](actions/create-feedback.md) | POST | Creates a new feedback item in Userback. |
| [Delete Feedback](actions/delete-feedback.md) | DELETE | Deletes a Userback feedback item. |
| [Get Feedback](actions/get-feedback.md) | GET | Retrieves a Userback feedback item by ID. |
| [List Feedbacks](actions/list-feedbacks.md) | GET | Lists the feedback items available in Userback. |
| [Update Feedback](actions/update-feedback.md) | PUT | Updates a Userback feedback item. |

### Feedback Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Feedback Comment](actions/create-feedback-comment.md) | POST | Creates a comment on a Userback feedback item. |
| [Delete Feedback Comment](actions/delete-feedback-comment.md) | DELETE | Deletes a Userback feedback comment. |
| [Get Feedback Comment](actions/get-feedback-comment.md) | GET | Retrieves a Userback feedback comment by ID. |
| [List Feedback Comments](actions/list-feedback-comments.md) | GET | Lists the comments for Userback feedback items. |
| [Update Feedback Comment](actions/update-feedback-comment.md) | PUT | Updates a Userback feedback comment. |

### Feedback Screenshot

| Action | Method | Description |
| --- | --- | --- |
| [Create Feedback Screenshot](actions/create-feedback-screenshot.md) | POST | Creates a screenshot for a Userback feedback item. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Get Member](actions/get-member.md) | GET | Retrieves a Userback member by ID. |
| [List Members](actions/list-members.md) | GET | Lists the members available in Userback. |
| [Update Member](actions/update-member.md) | PUT | Updates a Userback member. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a Userback project by ID. |
| [List Projects](actions/list-projects.md) | GET | Lists the projects available in Userback. |
| [Update Project](actions/update-project.md) | PUT | Updates a Userback project. |

### Session Recording

| Action | Method | Description |
| --- | --- | --- |
| [Get Session Recording](actions/get-session-recording.md) | GET | Retrieves a Userback session recording by ID. |
| [List Session Recordings](actions/list-session-recordings.md) | GET | Lists the session recordings available in Userback. |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Create Workflow](actions/create-workflow.md) | POST | Creates a new workflow in Userback. |
| [Delete Workflow](actions/delete-workflow.md) | DELETE | Deletes a workflow from Userback. |
| [List Workflows](actions/list-workflows.md) | GET | Lists the workflows available in Userback. |
| [Update Workflow](actions/update-workflow.md) | PUT | Updates a workflow in Userback. |

