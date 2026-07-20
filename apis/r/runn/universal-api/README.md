# <img src="https://images.mindcloud.co/apps/icons/images-31_1774902440174.png" alt="Runn logo" width="28" height="28"> Runn: Universal API

Runn is resource and project planning software for managing people, projects, allocations, capacity, time off, and utilization.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/runn/latest
- **Category:** Productivity / Project Management
- **Actions:** 42
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.runn.io
- **Vendor API docs:** https://developer.runn.io/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runn/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (42)

### Assignment

| Action | Method | Description |
| --- | --- | --- |
| [List Assignments](actions/list-assignments.md) | GET |  |
| [List Person Assignments](actions/list-person-assignments.md) | GET |  |
| [List Project Assignments](actions/list-project-assignments.md) | GET |  |

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Get Client](actions/get-client.md) | GET |  |
| [List Clients](actions/list-clients.md) | GET |  |

### Holiday

| Action | Method | Description |
| --- | --- | --- |
| [List Holiday Group Holidays](actions/list-holiday-group-holidays.md) | GET |  |

### Holiday Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Holiday Group](actions/get-holiday-group.md) | GET |  |
| [List Holiday Groups](actions/list-holiday-groups.md) | GET |  |

### Hour Report

| Action | Method | Description |
| --- | --- | --- |
| [List Person Hour Report](actions/list-person-hour-report.md) | GET |  |
| [List Project Hour Report](actions/list-project-hour-report.md) | GET |  |

### Milestone

| Action | Method | Description |
| --- | --- | --- |
| [List Milestones](actions/list-milestones.md) | GET |  |
| [List Project Milestones](actions/list-project-milestones.md) | GET |  |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Get Person](actions/get-person.md) | GET |  |
| [List People](actions/list-people.md) | GET |  |
| [List Project People](actions/list-project-people.md) | GET |  |
| [List Skill People](actions/list-skill-people.md) | GET |  |
| [List Team People](actions/list-team-people.md) | GET |  |

### Phase

| Action | Method | Description |
| --- | --- | --- |
| [List Project Phases](actions/list-project-phases.md) | GET |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET |  |
| [List Client Projects](actions/list-client-projects.md) | GET |  |
| [List Person Projects](actions/list-person-projects.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |

### Project Rate

| Action | Method | Description |
| --- | --- | --- |
| [List Project Rates](actions/list-project-rates.md) | GET |  |

### Project Total

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Total](actions/get-project-total.md) | GET |  |
| [List Project Totals](actions/list-project-totals.md) | GET |  |

### Rate Card

| Action | Method | Description |
| --- | --- | --- |
| [Get Rate Card](actions/get-rate-card.md) | GET |  |
| [List Rate Cards](actions/list-rate-cards.md) | GET |  |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [Get Role](actions/get-role.md) | GET |  |
| [List Roles](actions/list-roles.md) | GET |  |

### Skill

| Action | Method | Description |
| --- | --- | --- |
| [Get Skill](actions/get-skill.md) | GET |  |
| [List Person Skills](actions/list-person-skills.md) | GET |  |
| [List Skills](actions/list-skills.md) | GET |  |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Get Person Current Team](actions/get-person-current-team.md) | GET |  |
| [Get Team](actions/get-team.md) | GET |  |
| [List Teams](actions/list-teams.md) | GET |  |

### Time Off

| Action | Method | Description |
| --- | --- | --- |
| [List Person Holiday Time Off](actions/list-person-holiday-time-off.md) | GET |  |
| [List Person Leave Time Off](actions/list-person-leave-time-off.md) | GET |  |
| [List Person Rostered Off Time Off](actions/list-person-rostered-off-time-off.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |
| [Get User](actions/get-user.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |

### Workstream

| Action | Method | Description |
| --- | --- | --- |
| [List Project Workstreams](actions/list-project-workstreams.md) | GET |  |

