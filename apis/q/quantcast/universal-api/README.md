# <img src="https://images.mindcloud.co/apps/icons/quantcast-icon-512_1776361818026.png" alt="Quantcast logo" width="28" height="28"> Quantcast: Universal API

Quantcast GraphQL API access for organizations, accounts, campaigns, adsets, creatives, teams, surveys, geo resources, and reporting queries.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/quantcast/latest
- **Category:** Marketing / Advertising
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.quantcast.com
- **Vendor API docs:** https://developers.quantcast.com/docs/graphql-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organizations](actions/list-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Ad Groups

| Action | Method | Description |
| --- | --- | --- |
| [List Adsets](actions/list-adsets.md) | GET | Retrieves adsets from Quantcast. |

### Addresses

| Action | Method | Description |
| --- | --- | --- |
| [List Cities](actions/list-cities.md) | GET | Retrieves cities from Quantcast. |
| [List Countries](actions/list-countries.md) | GET | Retrieves countries from Quantcast. |
| [List Metro Areas](actions/list-metro-areas.md) | GET | Retrieves metro areas from Quantcast. |
| [List Postcodes](actions/list-postcodes.md) | GET | Retrieves postcodes from Quantcast. |
| [List States](actions/list-states.md) | GET | Retrieves states from Quantcast. |

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [List Creatives](actions/list-creatives.md) | GET | Retrieves creatives from Quantcast. |

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [List Key Events](actions/list-key-events.md) | GET | Retrieves key events from Quantcast. |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from Quantcast. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [List Surveys](actions/list-surveys.md) | GET | Retrieves surveys from Quantcast. |

### Mappings

| Action | Method | Description |
| --- | --- | --- |
| [List Creative Assignments](actions/list-creative-assignments.md) | GET | Retrieves creative assignments from Quantcast. |

### Memberships

| Action | Method | Description |
| --- | --- | --- |
| [List Team Members](actions/list-team-members.md) | GET | Retrieves team members from Quantcast. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from Quantcast. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Metrics Report](actions/get-account-metrics-report.md) | GET | Retrieves an account metrics report from Quantcast. |
| [Get Async Attributed Actions Report Download URL](actions/get-async-attributed-actions-report-download-url.md) | GET | Retrieves an async attributed actions report download URL from Quantcast. |
| [Get Async Metrics Report Download URL](actions/get-async-metrics-report-download-url.md) | GET | Retrieves an async metrics report download URL from Quantcast. |
| [Get Available Breakdowns And Metrics](actions/get-available-breakdowns-and-metrics.md) | GET | Retrieves available breakdowns and metrics from Quantcast. |
| [Request Async Attributed Actions Report](actions/request-async-attributed-actions-report.md) | POST | Requests an async attributed actions report from Quantcast. |
| [Request Async Metrics Report](actions/request-async-metrics-report.md) | POST | Requests an async metrics report from Quantcast. |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [List Roles](actions/list-roles.md) | GET | Retrieves roles from Quantcast. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams from Quantcast. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [List ISPs](actions/list-isps.md) | GET | Retrieves ISPs from Quantcast. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Members](actions/list-members.md) | GET | Retrieves organization members from Quantcast. |

### Viewer Assignments

| Action | Method | Description |
| --- | --- | --- |
| [List User Account Assignments](actions/list-user-account-assignments.md) | GET | Retrieves user account assignments from Quantcast. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accounts from Quantcast. |

