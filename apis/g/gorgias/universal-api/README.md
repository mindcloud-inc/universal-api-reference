# <img src="https://images.mindcloud.co/apps/icons/gorgias_1775166128245.png" alt="Gorgias logo" width="28" height="28"> Gorgias: Universal API

Connect Gorgias to read and manage support data including account, customers, tickets, users, tags, macros, rules, views, widgets, and related helpdesk resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gorgias/latest
- **Category:** Support / Ticketing
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.gorgias.com
- **Vendor API docs:** https://developers.gorgias.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Account](actions/retrieve-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Account](actions/retrieve-account.md) | GET | Retrieves account details from Gorgias. |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Finds custom fields in Gorgias. |
| [Retrieve Custom Field](actions/retrieve-custom-field.md) | GET | Retrieves a custom field from Gorgias. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [List Customers](actions/list-customers.md) | GET | Finds customers in Gorgias. |
| [Retrieve Customer](actions/retrieve-customer.md) | GET | Retrieves a customer from Gorgias. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET | Finds events in Gorgias. |
| [Retrieve Event](actions/retrieve-event.md) | GET | Retrieves an event from Gorgias. |

### Integration

| Action | Method | Description |
| --- | --- | --- |
| [List Integrations](actions/list-integrations.md) | GET | Finds integrations in Gorgias. |
| [Retrieve Integration](actions/retrieve-integration.md) | GET | Retrieves an integration from Gorgias. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [List Jobs](actions/list-jobs.md) | GET | Finds jobs in Gorgias. |
| [Retrieve Job](actions/retrieve-job.md) | GET | Retrieves a job from Gorgias. |

### Macro

| Action | Method | Description |
| --- | --- | --- |
| [List Macros](actions/list-macros.md) | GET | Finds macros in Gorgias. |
| [Retrieve Macro](actions/retrieve-macro.md) | GET | Retrieves a macro from Gorgias. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [List Messages](actions/list-messages.md) | GET | Finds messages in Gorgias. |

### Rule

| Action | Method | Description |
| --- | --- | --- |
| [List Rules](actions/list-rules.md) | GET | Finds rules in Gorgias. |
| [Retrieve Rule](actions/retrieve-rule.md) | GET | Retrieves a rule from Gorgias. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Resources](actions/search-resources.md) | GET | Finds resources in Gorgias by query. |

### Setting

| Action | Method | Description |
| --- | --- | --- |
| [List Settings](actions/list-settings.md) | GET | Finds account settings in Gorgias. |

### Survey

| Action | Method | Description |
| --- | --- | --- |
| [List Surveys](actions/list-surveys.md) | GET | Finds satisfaction surveys in Gorgias. |
| [Retrieve Survey](actions/retrieve-survey.md) | GET | Retrieves a satisfaction survey from Gorgias. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET | Finds tags in Gorgias. |
| [Retrieve Tag](actions/retrieve-tag.md) | GET | Retrieves a tag from Gorgias. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET | Finds teams in Gorgias. |
| [Retrieve Team](actions/retrieve-team.md) | GET | Retrieves a team from Gorgias. |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [List Tickets](actions/list-tickets.md) | GET | Finds tickets in Gorgias. |
| [Retrieve Ticket](actions/retrieve-ticket.md) | GET | Retrieves a ticket from Gorgias. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Finds users in Gorgias. |
| [Retrieve User](actions/retrieve-user.md) | GET | Retrieves a user from Gorgias. |

### View

| Action | Method | Description |
| --- | --- | --- |
| [List Views](actions/list-views.md) | GET | Finds views in Gorgias. |
| [Retrieve View](actions/retrieve-view.md) | GET | Retrieves a view from Gorgias. |

### Widget

| Action | Method | Description |
| --- | --- | --- |
| [List Widgets](actions/list-widgets.md) | GET | Finds widgets in Gorgias. |
| [Retrieve Widget](actions/retrieve-widget.md) | GET | Retrieves a widget from Gorgias. |

