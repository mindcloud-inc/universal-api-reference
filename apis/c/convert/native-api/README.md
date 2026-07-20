# Convert: Native API Reference

A consolidated summary of Convert's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://api.convert.com/doc/v2/
- **OpenAPI specification:** https://api.convert.com/doc/v2/
- **API base URL:** `https://api.convert.com/api/v2`

## Authentication

### Request-Signing API Key

Use Convert API request-signing credentials: account ID, application ID, and application secret.

### Credentials

- **Account ID:** `accountId` · required · Convert account ID used in account-scoped API paths.
- **API Key ID:** `apiKey` · required · Convert request-signing application ID. Used as the Convert-Application-ID header.
- **API Key Secret:** `apiKeySecret` · required · Convert request-signing application secret used to compute the HMAC SHA-256 signature.

[Official authentication documentation](https://api.convert.com/doc/v2/#section/Authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Retry behavior

Retry responses with status codes `408,409,425,429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Access Roles](actions/get-access-roles.md) | `GET /access-roles` | [docs](https://api.convert.com/doc/v2/#tag/User/operation/getAccessRoles) |
| [Get Account Details](actions/get-account-details.md) | `GET /accounts/:account_id/details` | [docs](https://api.convert.com/doc/v2/#tag/Accounts/operation/getAccountDetails) |
| [List Account User Accesses](actions/get-account-users-accesses-list.md) | `GET /accounts/:account_id/users-accesses` | [docs](https://api.convert.com/doc/v2/#tag/Collaborators/operation/getAccountUsersAccessesList) |
| [List Accounts](actions/get-accounts-list.md) | `GET /accounts` | [docs](https://api.convert.com/doc/v2/#tag/Accounts/operation/getAccountsList) |
| [Get Audience](actions/get-audience.md) | `GET /accounts/:account_id/projects/:project_id/audiences/:audience_id` | [docs](https://api.convert.com/doc/v2/#tag/Audiences/operation/getAudience) |
| [List Audiences](actions/get-audiences-list.md) | `POST /accounts/:account_id/projects/:project_id/audiences` | [docs](https://api.convert.com/doc/v2/#tag/Audiences/operation/getAudiencesList) |
| [List Billing Plans](actions/get-billing-plans.md) | `GET /billing-plans` | [docs](https://api.convert.com/doc/v2/#tag/Accounts/operation/getBillingPlans) |
| [Get Experience](actions/get-experience.md) | `GET /accounts/:account_id/projects/:project_id/experiences/:experience_id` | [docs](https://api.convert.com/doc/v2/#tag/Experiences/operation/getExperience) |
| [Get Experience Aggregated Report](actions/get-experience-aggregated-report.md) | `POST /accounts/:account_id/projects/:project_id/experiences/:experience_id/aggregated_report` | [docs](https://api.convert.com/doc/v2/#tag/Experiences-Reports/operation/getExperienceAggregatedReport) |
| [Get Experience By Key](actions/get-experience-by-key.md) | `GET /accounts/:account_id/projects/:project_id/experiences/:experience_key` | [docs](https://api.convert.com/doc/v2/#tag/Experiences/operation/getExperienceByKey) |
| [Get Experience Report Settings](actions/get-experience-report-settings.md) | `GET /accounts/:account_id/projects/:project_id/experiences/:experience_id/report_settings` | [docs](https://api.convert.com/doc/v2/#tag/Experiences-Reports/operation/getExperienceReportSettings) |
| [List Experiences](actions/get-experiences-list.md) | `POST /accounts/:account_id/projects/:project_id/experiences` | [docs](https://api.convert.com/doc/v2/#tag/Experiences/operation/getExperiencesList) |
| [Get Goal](actions/get-goal.md) | `GET /accounts/:account_id/projects/:project_id/goals/:goal_id` | [docs](https://api.convert.com/doc/v2/#tag/Goals/operation/getGoal) |
| [Get Goal By Key](actions/get-goal-by-key.md) | `GET /accounts/:account_id/projects/:project_id/goals/:goal_key` | [docs](https://api.convert.com/doc/v2/#tag/Goals/operation/getGoalByKey) |
| [List Goals](actions/get-goals-list.md) | `POST /accounts/:account_id/projects/:project_id/goals` | [docs](https://api.convert.com/doc/v2/#tag/Goals/operation/getGoalsList) |
| [List Hypotheses](actions/get-hypotheses-list.md) | `POST /accounts/:account_id/projects/:project_id/hypotheses` | [docs](https://api.convert.com/doc/v2/#tag/Hypotheses/operation/getHypothesesList) |
| [Get Hypothesis](actions/get-hypothesis.md) | `GET /accounts/:account_id/projects/:project_id/hypotheses/:hypothesis_id` | [docs](https://api.convert.com/doc/v2/#tag/Hypotheses/operation/getHypothesis) |
| [Get Knowledge Base Entry](actions/get-knowledge-base.md) | `GET /accounts/:account_id/projects/:project_id/knowledge-bases/:knowledge_base_id` | [docs](https://api.convert.com/doc/v2/#tag/Knowledge-Bases/operation/getKnowledgeBase) |
| [List Knowledge Base Entries](actions/get-knowledge-bases-list.md) | `POST /accounts/:account_id/projects/:project_id/knowledge-bases` | [docs](https://api.convert.com/doc/v2/#tag/Knowledge-Bases/operation/getKnowledgeBasesList) |
| [Get Location](actions/get-location.md) | `GET /accounts/:account_id/projects/:project_id/locations/:location_id` | [docs](https://api.convert.com/doc/v2/#tag/Locations/operation/getLocation) |
| [List Locations](actions/get-locations-list.md) | `POST /accounts/:account_id/projects/:project_id/locations` | [docs](https://api.convert.com/doc/v2/#tag/Locations/operation/getLocationsList) |
| [Get Observation](actions/get-observation.md) | `GET /accounts/:account_id/projects/:project_id/observations/:observation_id` | [docs](https://api.convert.com/doc/v2/#tag/Observations/operation/getObservation) |
| [List Observations](actions/get-observations-list.md) | `POST /accounts/:account_id/projects/:project_id/observations` | [docs](https://api.convert.com/doc/v2/#tag/Observations/operation/getObservationsList) |
| [Get Project](actions/get-project.md) | `GET /accounts/:account_id/projects/:project_id` | [docs](https://api.convert.com/doc/v2/#tag/Projects/operation/getProject) |
| [Get Project History](actions/get-project-history.md) | `POST /accounts/:account_id/projects/:project_id/change-history` | [docs](https://api.convert.com/doc/v2/#tag/Projects/operation/getProjectHistory) |
| [Get Project Live Data](actions/get-project-live-data.md) | `POST /accounts/:account_id/projects/:project_id/livedata` | [docs](https://api.convert.com/doc/v2/#tag/Projects/operation/getProjectLiveData) |
| [List Projects](actions/get-projects-list.md) | `POST /accounts/:account_id/projects` | [docs](https://api.convert.com/doc/v2/#tag/Projects/operation/getProjectsList) |
| [List SDK Keys](actions/get-sdk-keys-list.md) | `GET /accounts/:account_id/projects/:project_id/sdk-keys` | [docs](https://api.convert.com/doc/v2/#tag/SDK-Keys/operation/getSdkKeysList) |
| [Get Current User](actions/get-user-data.md) | `GET /user` | [docs](https://api.convert.com/doc/v2/#tag/User/operation/getUserData) |
| [List API Keys](actions/list-api-keys.md) | `GET /accounts/:account_id/api-keys` | [docs](https://api.convert.com/doc/v2/#tag/API-Keys/operation/listAPIKeys) |
