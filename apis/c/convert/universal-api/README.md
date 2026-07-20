# <img src="https://images.mindcloud.co/apps/icons/icon128x128_1776896191826.jpeg" alt="Convert logo" width="28" height="28"> Convert: Universal API

Convert Experiences API wrapper for accounts, projects, experiences, domains, visitors, reports, goals, audiences, and account administration.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/convert/latest
- **Category:** Marketing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.convert.com/
- **Vendor API docs:** https://api.convert.com/doc/v2/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List API Keys](actions/list-api-keys.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convert/latest/actions/list-api-keys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Access Role

| Action | Method | Description |
| --- | --- | --- |
| [List Access Roles](actions/get-access-roles.md) | GET | Retrieves available access roles from Convert. |

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Details](actions/get-account-details.md) | GET | Retrieves detailed account information from Convert. |
| [List Accounts](actions/get-accounts-list.md) | GET | Retrieves the available accounts from Convert. |

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [List API Keys](actions/list-api-keys.md) | GET | Retrieves API keys from Convert for an account. |

### Audience

| Action | Method | Description |
| --- | --- | --- |
| [Get Audience](actions/get-audience.md) | GET | Retrieves an audience from a Convert project. |
| [List Audiences](actions/get-audiences-list.md) | GET | Retrieves audiences from a Convert project. |

### Billing Plan

| Action | Method | Description |
| --- | --- | --- |
| [List Billing Plans](actions/get-billing-plans.md) | GET | Retrieves available billing plans from Convert. |

### Experience

| Action | Method | Description |
| --- | --- | --- |
| [Get Experience](actions/get-experience.md) | GET | Retrieves an experience from a Convert project. |
| [Get Experience By Key](actions/get-experience-by-key.md) | GET | Retrieves an experience from Convert by key. |
| [List Experiences](actions/get-experiences-list.md) | GET | Retrieves experiences from a Convert project. |

### Experience Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Experience Aggregated Report](actions/get-experience-aggregated-report.md) | GET | Retrieves an aggregated report for a Convert experience. |

### Experience Report Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Experience Report Settings](actions/get-experience-report-settings.md) | GET | Retrieves report settings for a Convert experience. |

### Goal

| Action | Method | Description |
| --- | --- | --- |
| [Get Goal](actions/get-goal.md) | GET | Retrieves a goal from a Convert project. |
| [Get Goal By Key](actions/get-goal-by-key.md) | GET | Retrieves a goal from Convert by key. |
| [List Goals](actions/get-goals-list.md) | GET | Retrieves goals from a Convert project. |

### Hypothesis

| Action | Method | Description |
| --- | --- | --- |
| [List Hypotheses](actions/get-hypotheses-list.md) | GET | Retrieves hypotheses from a Convert project. |
| [Get Hypothesis](actions/get-hypothesis.md) | GET | Retrieves a hypothesis from a Convert project. |

### Knowledge Base Entry

| Action | Method | Description |
| --- | --- | --- |
| [Get Knowledge Base Entry](actions/get-knowledge-base.md) | GET | Retrieves a knowledge base entry from Convert. |
| [List Knowledge Base Entries](actions/get-knowledge-bases-list.md) | GET | Retrieves knowledge base entries from a Convert project. |

### Live Data Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Live Data](actions/get-project-live-data.md) | GET | Retrieves live data for a Convert project. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Get Location](actions/get-location.md) | GET | Retrieves a location from a Convert project. |
| [List Locations](actions/get-locations-list.md) | GET | Retrieves locations from a Convert project. |

### Observation

| Action | Method | Description |
| --- | --- | --- |
| [Get Observation](actions/get-observation.md) | GET | Retrieves an observation from a Convert project. |
| [List Observations](actions/get-observations-list.md) | GET | Retrieves observations from a Convert project. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from a Convert account. |
| [List Projects](actions/get-projects-list.md) | GET | Retrieves projects from a Convert account. |

### Project History Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Project History](actions/get-project-history.md) | GET | Retrieves project change history from Convert. |

### Sdk Key

| Action | Method | Description |
| --- | --- | --- |
| [List SDK Keys](actions/get-sdk-keys-list.md) | GET | Retrieves SDK keys from a Convert project. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-user-data.md) | GET | Retrieves the current user from Convert. |

### User Access

| Action | Method | Description |
| --- | --- | --- |
| [List Account User Accesses](actions/get-account-users-accesses-list.md) | GET | Retrieves user access entries for a Convert account. |

