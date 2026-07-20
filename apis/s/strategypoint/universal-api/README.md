# <img src="https://images.mindcloud.co/apps/icons/strategypoint-icon_1775486604090.png" alt="Strategypoint logo" width="28" height="28"> Strategypoint: Universal API

ClearPoint Strategy API access for scorecards, objectives, measures, initiatives, action items, risks, reports, users, and related strategic planning resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/strategypoint/latest
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.clearpointstrategy.com/
- **Vendor API docs:** https://developer.clearpointstrategy.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Scorecards](actions/list-scorecards.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-scorecards?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Actions

| Action | Method | Description |
| --- | --- | --- |
| [Get Action Item](actions/get-action-item.md) | GET | Retrieves an action item from Strategypoint. |
| [List Action Items](actions/list-action-items.md) | GET | Retrieves action items from Strategypoint. |

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Get Attachment](actions/get-attachment.md) | GET | Retrieves an attachment from Strategypoint. |
| [List Attachments](actions/list-attachments.md) | GET | Retrieves attachments from Strategypoint. |

### Favorite

| Action | Method | Description |
| --- | --- | --- |
| [Check Favorite](actions/check-favorite.md) | GET | Checks favorites in Strategypoint. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Get File](actions/get-file.md) | GET | Retrieves a file from Strategypoint. |
| [List Files](actions/list-files.md) | GET | Retrieves files from Strategypoint. |

### Goal

| Action | Method | Description |
| --- | --- | --- |
| [Get Goal](actions/get-goal.md) | GET | Retrieves a goal from Strategypoint. |
| [List Goals](actions/list-goals.md) | GET | Retrieves goals from Strategypoint. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from Strategypoint. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from Strategypoint. |

### Initiative

| Action | Method | Description |
| --- | --- | --- |
| [Get Initiative](actions/get-initiative.md) | GET | Retrieves an initiative from Strategypoint. |
| [List Initiatives](actions/list-initiatives.md) | GET | Retrieves initiatives from Strategypoint. |

### Measure

| Action | Method | Description |
| --- | --- | --- |
| [Get Measure](actions/get-measure.md) | GET | Retrieves a measure from Strategypoint. |
| [List Measures](actions/list-measures.md) | GET | Retrieves measures from Strategypoint. |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [Get Notification](actions/get-notification.md) | GET | Retrieves a notification from Strategypoint. |
| [List Notifications](actions/list-notifications.md) | GET | Retrieves notifications from Strategypoint. |

### Objectives

| Action | Method | Description |
| --- | --- | --- |
| [Get Objective](actions/get-objective.md) | GET | Retrieves an objective from Strategypoint. |
| [List Objectives](actions/list-objectives.md) | GET | Retrieves objectives from Strategypoint. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Report](actions/get-report.md) | GET | Retrieves a report from Strategypoint. |
| [List Reports](actions/list-reports.md) | GET | Retrieves reports from Strategypoint. |

### Risk

| Action | Method | Description |
| --- | --- | --- |
| [Get Risk](actions/get-risk.md) | GET | Retrieves a risk from Strategypoint. |
| [List Risks](actions/list-risks.md) | GET | Retrieves risks from Strategypoint. |

### Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Get Schedule](actions/get-schedule.md) | GET | Retrieves a schedule from Strategypoint. |
| [List Schedules](actions/list-schedules.md) | GET | Retrieves schedules from Strategypoint. |

### Scorecards

| Action | Method | Description |
| --- | --- | --- |
| [Get Scorecard](actions/get-scorecard.md) | GET | Retrieves a scorecard from Strategypoint. |
| [List Scorecards](actions/list-scorecards.md) | GET | Retrieves scorecards from Strategypoint. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search](actions/search.md) | GET | Finds matching elements in Strategypoint. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Strategypoint. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Strategypoint. |

