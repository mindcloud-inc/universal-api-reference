# <img src="https://images.mindcloud.co/apps/icons/idar-qeta-ks-logos_1775842369506.jpeg" alt="4HSE logo" width="28" height="28"> 4HSE: Universal API

Manage workplace safety deadlines, risks, and activities

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hSE/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.4hse.com/en
- **Vendor API docs:** https://docs.4hse.com/en/dev/guides/using-rest-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Action Sessions](actions/list-action-sessions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-action-sessions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Action

| Action | Method | Description |
| --- | --- | --- |
| [Create Action](actions/create-action.md) | POST | Creates a new action in 4HSE. |
| [List Actions](actions/list-actions.md) | GET | Retrieves actions from 4HSE. |
| [Update Action](actions/update-action.md) | PUT | Updates an existing action in 4HSE. |
| [View Action](actions/view-action.md) | GET | Retrieves an action from 4HSE. |

### Action Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Action Session](actions/create-action-session.md) | POST | Creates a new action session in 4HSE. |
| [List Action Sessions](actions/list-action-sessions.md) | GET | Retrieves action sessions from 4HSE. |
| [Update Action Session](actions/update-action-session.md) | PUT | Updates an existing action session in 4HSE. |

### Action Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Action Subscription](actions/create-action-subscription.md) | POST | Creates a new action subscription in 4HSE. |
| [List Action Subscriptions](actions/list-action-subscriptions.md) | GET | Retrieves action subscriptions from 4HSE. |
| [Update Action Subscription](actions/update-action-subscription.md) | PUT | Updates an existing action subscription in 4HSE. |

### Certificate

| Action | Method | Description |
| --- | --- | --- |
| [Create Certificate](actions/create-certificate.md) | POST | Creates a new certificate in 4HSE. |
| [List Certificates](actions/list-certificates.md) | GET | Retrieves certificates from 4HSE. |
| [Update Certificate](actions/update-certificate.md) | PUT | Updates an existing certificate in 4HSE. |
| [View Certificate](actions/view-certificate.md) | GET | Retrieves a certificate from 4HSE. |

### Certificate Action Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Certificate Action Link](actions/create-certificate-action-link.md) | POST | Creates a new certificate-action link in 4HSE. |
| [List Certificate Action Links](actions/list-certificate-action-links.md) | GET | Retrieves certificate-action links from 4HSE. |

### Demand

| Action | Method | Description |
| --- | --- | --- |
| [Create Demand](actions/create-demand.md) | POST | Creates a new demand in 4HSE. |

### Equipment

| Action | Method | Description |
| --- | --- | --- |
| [List Equipment](actions/list-equipment.md) | GET | Retrieves equipment from 4HSE. |

### Incident

| Action | Method | Description |
| --- | --- | --- |
| [Create Incident](actions/create-incident.md) | POST | Creates a new incident in 4HSE. |
| [List Incidents](actions/list-incidents.md) | GET | Retrieves incidents from 4HSE. |

### Office

| Action | Method | Description |
| --- | --- | --- |
| [Create Office](actions/create-office.md) | POST | Creates a new office in 4HSE. |
| [List Offices](actions/list-offices.md) | GET | Retrieves offices from 4HSE. |
| [Update Office](actions/update-office.md) | PUT | Updates an existing office in 4HSE. |
| [View Office](actions/view-office.md) | GET | Retrieves an office from 4HSE. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Create Person](actions/create-person.md) | POST | Creates a new person in 4HSE. |
| [Historicize Person](actions/historicize-person.md) | PUT | Updates an existing person in 4HSE by historicizing it. |
| [List People](actions/list-people.md) | GET | Retrieves people from 4HSE. |
| [Update Person](actions/update-person.md) | PUT | Updates an existing person in 4HSE. |
| [View Person](actions/view-person.md) | GET | Retrieves a person from 4HSE. |

### Personoffice Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Create PersonOffice Assignment](actions/create-person-office-assignment.md) | POST | Creates a new person-office assignment in 4HSE. |
| [List PersonOffice Assignments](actions/list-person-office-assignments.md) | GET | Retrieves person-office assignments from 4HSE. |
| [Update PersonOffice Assignment](actions/update-person-office-assignment.md) | PUT | Updates an existing person-office assignment in 4HSE. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in 4HSE. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from 4HSE. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in 4HSE. |

### Session Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Session Subscription](actions/create-session-subscription.md) | POST | Creates a new session subscription in 4HSE. |
| [List Session Subscriptions](actions/list-session-subscriptions.md) | GET | Retrieves session subscriptions from 4HSE. |

### Work Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Work Group](actions/create-work-group.md) | POST | Creates a new work group in 4HSE. |
| [List Work Groups](actions/list-work-groups.md) | GET | Retrieves work groups from 4HSE. |

### Work Group Person

| Action | Method | Description |
| --- | --- | --- |
| [Assign Person To Work Group](actions/assign-person-to-work-group.md) | POST | Creates a new work group assignment in 4HSE. |

