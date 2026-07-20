# <img src="https://images.mindcloud.co/apps/icons/unnamed_1773347580409.png" alt="SafetyCulture logo" width="28" height="28"> SafetyCulture: Universal API

Run inspections, manage actions, and resolve issues in SafetyCulture

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/safetyCulture/latest
- **Category:** Support / Field Service
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://safetyculture.com
- **Vendor API docs:** https://developer.safetyculture.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Groups and Organizations](actions/list-groups-and-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/list-groups-and-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Action

| Action | Method | Description |
| --- | --- | --- |
| [Create Action](actions/create-action.md) | POST | Creates a new action in SafetyCulture. |
| [Get Action](actions/get-action.md) | GET | Retrieves an action from SafetyCulture. |
| [List Actions](actions/list-actions.md) | GET | Retrieves actions from SafetyCulture. |

### Action Assignees

| Action | Method | Description |
| --- | --- | --- |
| [Update Action Assignees](actions/update-action-assignees.md) | PUT | Updates action assignees in SafetyCulture. |

### Action Due Date

| Action | Method | Description |
| --- | --- | --- |
| [Update Action Due Date](actions/update-action-due-date.md) | PUT | Updates an action due date in SafetyCulture. |

### Action Priority

| Action | Method | Description |
| --- | --- | --- |
| [Update Action Priority](actions/update-action-priority.md) | PUT | Updates an action priority in SafetyCulture. |

### Action Status

| Action | Method | Description |
| --- | --- | --- |
| [Update Action Status](actions/update-action-status.md) | PUT | Updates an action status in SafetyCulture. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [List Groups and Organizations](actions/list-groups-and-organizations.md) | GET | Retrieves groups and organizations from SafetyCulture. |

### Inspection

| Action | Method | Description |
| --- | --- | --- |
| [Get Inspection](actions/get-inspection.md) | GET | Retrieves an inspection from SafetyCulture. |
| [Search Modified Inspections](actions/search-modified-inspections.md) | GET | Finds modified inspections in SafetyCulture. |
| [Start Inspection](actions/start-inspection.md) | POST | Creates a new inspection in SafetyCulture. |
| [Update Inspection](actions/update-inspection.md) | PUT | Updates an inspection in SafetyCulture. |

### Inspection Answers

| Action | Method | Description |
| --- | --- | --- |
| [Get Inspection Answers](actions/get-inspection-answers.md) | GET | Retrieves inspection answers from SafetyCulture. |

### Inspection Completion

| Action | Method | Description |
| --- | --- | --- |
| [Complete Inspection](actions/complete-inspection.md) | PUT | Completes an inspection in SafetyCulture. |

### Inspection Deep Link

| Action | Method | Description |
| --- | --- | --- |
| [Generate Inspection Deep Link](actions/generate-inspection-deep-link.md) | GET | Generates an inspection deep link in SafetyCulture. |

### Inspection Details

| Action | Method | Description |
| --- | --- | --- |
| [Get Inspection Details](actions/get-inspection-details.md) | GET | Retrieves inspection details from SafetyCulture. |

### Inspection Media

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Selected Media](actions/retrieve-selected-media.md) | GET | Retrieves selected inspection media from SafetyCulture. |

### Inspection Owner

| Action | Method | Description |
| --- | --- | --- |
| [Set Inspection Owner](actions/set-inspection-owner.md) | PUT | Updates an inspection owner in SafetyCulture. |

### Inspection Site

| Action | Method | Description |
| --- | --- | --- |
| [Set Inspection Site](actions/set-inspection-site.md) | PUT | Updates an inspection site in SafetyCulture. |

### Inspection Web Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Inspection Web Report Link](actions/get-inspection-web-report-link.md) | GET | Retrieves an inspection web report link from SafetyCulture. |

### Issue

| Action | Method | Description |
| --- | --- | --- |
| [Create Issue](actions/create-issue.md) | POST | Creates a new issue in SafetyCulture. |
| [Get Issue](actions/get-issue.md) | GET | Retrieves an issue from SafetyCulture. |
| [List Issues](actions/list-issues.md) | GET | Retrieves issues from SafetyCulture. |

### Issue Comment

| Action | Method | Description |
| --- | --- | --- |
| [Add Comment to Issue Timeline](actions/add-comment-to-issue-timeline.md) | POST | Creates an issue timeline comment in SafetyCulture. |

### Issue Status

| Action | Method | Description |
| --- | --- | --- |
| [Update Issue Status](actions/update-issue-status.md) | PUT | Updates an issue status in SafetyCulture. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from SafetyCulture. |
| [Get Template by Inspection](actions/get-template-by-inspection.md) | GET | Retrieves a template by inspection in SafetyCulture. |
| [Search Modified Templates](actions/search-modified-templates.md) | GET | Finds modified templates in SafetyCulture. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in SafetyCulture. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from SafetyCulture. |

