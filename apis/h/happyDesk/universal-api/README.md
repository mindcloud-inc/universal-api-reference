# <img src="https://images.mindcloud.co/apps/icons/fav_1777490137096.png" alt="HappyDesk logo" width="28" height="28"> HappyDesk: Universal API

HappyDesk is a helpdesk and ticketing platform for customer and employee support, with omnichannel requests, automation, a knowledge base, and a customer portal.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/happyDesk/latest
- **Category:** Support / Ticketing
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://happydesk.ru/
- **Vendor API docs:** https://staffy.happydesk.ru/api-docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Company Settings](actions/get-company-settings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/happyDesk/latest/actions/get-company-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Settings](actions/get-company-settings.md) | GET |  |

### Current User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |

### Issue

| Action | Method | Description |
| --- | --- | --- |
| [Get Issues](actions/get-issues.md) | GET |  |

### Issue Category Tree

| Action | Method | Description |
| --- | --- | --- |
| [Get Nested Issue Categories](actions/get-nested-issue-categories.md) | GET |  |

### Issue Channel

| Action | Method | Description |
| --- | --- | --- |
| [Get Issue Channels](actions/get-issue-channels.md) | GET |  |

### Issue Priority

| Action | Method | Description |
| --- | --- | --- |
| [Get Issue Priorities](actions/get-issue-priorities.md) | GET |  |

### Issue Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Issue Statuses](actions/get-issue-statuses.md) | GET |  |

### Issue Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Issue Templates](actions/get-issue-templates.md) | GET |  |

### Issue Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Issue Types](actions/get-issue-types.md) | GET |  |

### Knowledge Category

| Action | Method | Description |
| --- | --- | --- |
| [Get All Knowledge Categories](actions/get-all-knowledge-categories.md) | GET |  |
| [Get Knowledge Categories](actions/get-knowledge-categories.md) | GET |  |

### Knowledge Instruction

| Action | Method | Description |
| --- | --- | --- |
| [Get All Knowledge Instructions](actions/get-all-knowledge-instructions.md) | GET |  |
| [Get Knowledge Instructions](actions/get-knowledge-instructions.md) | GET |  |

### Knowledge Section

| Action | Method | Description |
| --- | --- | --- |
| [Get All Knowledge Sections](actions/get-all-knowledge-sections.md) | GET |  |
| [Get Knowledge Sections](actions/get-knowledge-sections.md) | GET |  |

### Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Get Schedules](actions/get-schedules.md) | GET |  |

### System Environment

| Action | Method | Description |
| --- | --- | --- |
| [Get System Environments](actions/get-system-environments.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Users](actions/get-users.md) | GET |  |

### User Company

| Action | Method | Description |
| --- | --- | --- |
| [Get User Company](actions/get-user-company.md) | GET |  |

### User Group

| Action | Method | Description |
| --- | --- | --- |
| [Get User Groups](actions/get-user-groups.md) | GET |  |

