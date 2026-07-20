# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-04-24-as-13_1777046766876.png" alt="Status Hero logo" width="28" height="28"> Status Hero: Universal API

Connect to Status Hero to retrieve team members, reports, check-ins, tags, comments, reactions, and manage absences or status activities.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/statusHero/latest
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://statushero.com
- **Vendor API docs:** https://api.statushero.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List members](actions/list-members.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/list-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Get comment](actions/get-comment.md) | GET |  |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Get member](actions/get-member.md) | GET |  |
| [List members](actions/list-members.md) | GET |  |

### Member Absence

| Action | Method | Description |
| --- | --- | --- |
| [Add member absence](actions/add-member-absence.md) | POST |  |
| [Remove member absence](actions/remove-member-absence.md) | DELETE |  |

### Reaction

| Action | Method | Description |
| --- | --- | --- |
| [Get reaction](actions/get-reaction.md) | GET |  |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get report](actions/get-report.md) | GET |  |
| [List reports](actions/list-reports.md) | GET |  |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Get status](actions/get-status.md) | GET |  |
| [List statuses](actions/list-statuses.md) | GET |  |
| [List statuses by tag](actions/list-statuses-by-tag.md) | GET |  |

### Status Activity

| Action | Method | Description |
| --- | --- | --- |
| [Add status activity](actions/add-status-activity.md) | POST |  |
| [Get status activity](actions/get-status-activity.md) | GET |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List tags](actions/list-tags.md) | GET |  |

### Team Absence

| Action | Method | Description |
| --- | --- | --- |
| [Add team absence](actions/add-team-absence.md) | POST |  |
| [Remove team absence](actions/remove-team-absence.md) | DELETE |  |

