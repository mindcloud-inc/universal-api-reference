# <img src="https://images.mindcloud.co/apps/icons/t-opdesk_1775165856397.png" alt="TOPdesk logo" width="28" height="28"> TOPdesk: Universal API

Manage service tickets, assets, and self-service workflows in TOPdesk.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tOPdesk/latest
- **Category:** Support / Ticketing
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.topdesk.com
- **Vendor API docs:** https://developers.topdesk.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Incident Statuses](actions/list-incident-statuses.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tOPdesk/latest/actions/list-incident-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Incident

| Action | Method | Description |
| --- | --- | --- |
| [Add Incident Time Spent](actions/add-incident-time-spent.md) | POST | Creates a time spent entry for an incident in TOPdesk. |
| [Archive Incident by ID](actions/archive-incident-by-id.md) | PUT | Archives an incident in TOPdesk by ID. |
| [Create Incident](actions/create-incident.md) | POST | Creates a new incident in TOPdesk. |
| [Deescalate Incident by ID](actions/deescalate-incident-by-id.md) | PUT | Deescalates an incident in TOPdesk by ID. |
| [Escalate Incident by ID](actions/escalate-incident-by-id.md) | PUT | Escalates an incident in TOPdesk by ID. |
| [Get Incident by ID](actions/get-incident-by-id.md) | GET | Retrieves an incident from TOPdesk by ID. |
| [Get Incident by Number](actions/get-incident-by-number.md) | GET | Retrieves an incident from TOPdesk by number. |
| [Get Incident Progress Trail Count](actions/get-incident-progress-trail-count.md) | GET | Retrieves an incident progress trail count from TOPdesk. |
| [Get Incident Time Spent](actions/get-incident-time-spent.md) | GET | Retrieves time spent for an incident from TOPdesk. |
| [List Deescalation Reasons](actions/list-deescalation-reasons.md) | GET | Retrieves incident deescalation reasons from TOPdesk. |
| [List Escalation Reasons](actions/list-escalation-reasons.md) | GET | Retrieves incident escalation reasons from TOPdesk. |
| [List Incident Actions](actions/list-incident-actions.md) | GET | Retrieves actions for an incident from TOPdesk. |
| [List Incident Call Types](actions/list-incident-call-types.md) | GET | Retrieves incident call types from TOPdesk. |
| [List Incident Categories](actions/list-incident-categories.md) | GET | Retrieves incident categories from TOPdesk. |
| [List Incident Priorities](actions/list-incident-priorities.md) | GET | Retrieves available incident priorities from TOPdesk. |
| [List Incident Progress Trail](actions/list-incident-progress-trail.md) | GET | Retrieves the progress trail for an incident from TOPdesk. |
| [List Incident Requests](actions/list-incident-requests.md) | GET | Retrieves requests for an incident from TOPdesk. |
| [List Incident Statuses](actions/list-incident-statuses.md) | GET | Retrieves available incident statuses from TOPdesk. |
| [List Incident Subcategories](actions/list-incident-subcategories.md) | GET | Retrieves incident subcategories from TOPdesk. |
| [List Incident Urgencies](actions/list-incident-urgencies.md) | GET | Retrieves available incident urgencies from TOPdesk. |
| [List Incidents](actions/list-incidents.md) | GET | Retrieves a list of incidents from TOPdesk. |
| [Replace Incident by ID](actions/replace-incident-by-id.md) | PUT | Replaces an existing incident in TOPdesk by ID. |
| [Replace Incident by Number](actions/replace-incident-by-number.md) | PUT | Replaces an existing incident in TOPdesk by number. |
| [Unarchive Incident by ID](actions/unarchive-incident-by-id.md) | PUT | Unarchives an incident in TOPdesk by ID. |
| [Update Incident by ID (Patch)](actions/update-incident-by-id-patch.md) | PUT | Updates an incident in TOPdesk by ID. |
| [Update Incident by Number (Patch)](actions/update-incident-by-number-patch.md) | PUT | Updates an incident in TOPdesk by number. |

