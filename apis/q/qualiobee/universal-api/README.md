# <img src="https://images.mindcloud.co/apps/icons/qualiobee_1774907323366.jpeg" alt="Qualiobee logo" width="28" height="28"> Qualiobee: Universal API

Manage training sessions, learners, customers, and compliance workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/qualiobee/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.qualiobee.fr/
- **Vendor API docs:** https://app.qualiobee.fr/api/doc/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Customers](actions/list-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Convention

| Action | Method | Description |
| --- | --- | --- |
| [Get Convention](actions/get-convention.md) | GET | Retrieves a convention from Qualiobee. |
| [List Conventions](actions/list-conventions.md) | GET | Retrieves conventions from Qualiobee. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Qualiobee. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Qualiobee. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Qualiobee. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in Qualiobee. |

### Formation

| Action | Method | Description |
| --- | --- | --- |
| [Create Formation](actions/create-formation.md) | POST | Creates a new formation in Qualiobee. |
| [Get Formation](actions/get-formation.md) | GET | Retrieves a formation from Qualiobee. |
| [List Formations](actions/list-formations.md) | GET | Retrieves formations from Qualiobee. |
| [Update Formation](actions/update-formation.md) | PUT | Updates an existing formation in Qualiobee. |

### Learner

| Action | Method | Description |
| --- | --- | --- |
| [Create Learner](actions/create-learner.md) | POST | Creates a new learner in Qualiobee. |
| [Get Learner](actions/get-learner.md) | GET | Retrieves a learner from Qualiobee. |
| [List Learners](actions/list-learners.md) | GET | Retrieves learners from Qualiobee. |
| [Update Learner](actions/update-learner.md) | PUT | Updates an existing learner in Qualiobee. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Create Location](actions/create-location.md) | POST | Creates a new location in Qualiobee. |
| [Get Location](actions/get-location.md) | GET | Retrieves a location from Qualiobee. |
| [List Locations](actions/list-locations.md) | GET | Retrieves locations from Qualiobee. |
| [Update Location](actions/update-location.md) | PUT | Updates an existing location in Qualiobee. |

### Qualiobee

| Action | Method | Description |
| --- | --- | --- |
| [Get Qualiobee Account](actions/get-qualiobee-account.md) | GET | Retrieves a Qualiobee account by UUID. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Session](actions/create-session.md) | POST | Creates a new session in Qualiobee. |
| [Get Session](actions/get-session.md) | GET | Retrieves a session from Qualiobee. |
| [List Sessions](actions/list-sessions.md) | GET | Retrieves sessions from Qualiobee. |
| [Start Session](actions/start-session.md) | PUT | Starts an existing session in Qualiobee. |
| [Update Session](actions/update-session.md) | PUT | Updates an existing session in Qualiobee. |

