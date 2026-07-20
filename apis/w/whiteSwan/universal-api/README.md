# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-04-08-as-14_1775668230114.png" alt="White Swan logo" width="28" height="28"> White Swan: Universal API

White Swan is a digital insurance brokerage platform for partners. Use it to start plan requests, retrieve client and plan data, start applications, and track earnings events.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/whiteSwan/latest
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.whiteswan.io/
- **Vendor API docs:** https://docs.whiteswan.io/partner-knowledge-base/api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Account Users](actions/list-account-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/list-account-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Account User

| Action | Method | Description |
| --- | --- | --- |
| [List Account Users](actions/list-account-users.md) | GET | Retrieves account users from White Swan. |

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Start Application](actions/start-application.md) | POST | Starts an application for a White Swan personal plan. |

### Case Party

| Action | Method | Description |
| --- | --- | --- |
| [Add Case Party](actions/add-case-party.md) | POST | Adds a case party to a White Swan case. |

### Earnings Event

| Action | Method | Description |
| --- | --- | --- |
| [List Earnings Events](actions/list-earnings-events.md) | GET | Retrieves earnings events from White Swan. |

### Personal Plan

| Action | Method | Description |
| --- | --- | --- |
| [List Personal Plans](actions/list-personal-plans.md) | GET | Retrieves personal plans from White Swan. |

### Plan Request

| Action | Method | Description |
| --- | --- | --- |
| [List Plan Requests](actions/list-plan-requests.md) | GET | Retrieves plan requests from White Swan. |
| [Start Personal Plan Request](actions/start-personal-plan-request.md) | POST | Starts a personal plan request in White Swan. |
| [Submit Complete Plan Request](actions/submit-complete-plan-request.md) | POST | Submits a complete personal plan request in White Swan. |

### Policy Search

| Action | Method | Description |
| --- | --- | --- |
| [Policy Search](actions/policy-search.md) | GET | Retrieves a White Swan policy search by ID. |

### Pre-fill Information

| Action | Method | Description |
| --- | --- | --- |
| [Create Pre-Fill Information](actions/create-pre-fill-information.md) | POST | Creates application pre-fill information in White Swan. |

### Referred Client

| Action | Method | Description |
| --- | --- | --- |
| [List Referred Clients](actions/list-referred-clients.md) | GET | Retrieves referred clients from White Swan. |

