# <img src="https://images.mindcloud.co/apps/icons/snyk_1776264927054.png" alt="Snyk logo" width="28" height="28"> Snyk: Universal API

Snyk is a developer security platform for managing organizations, projects, issues, targets, integrations, and reporting through the Snyk REST and v1 APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/snyk/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 60
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://snyk.io
- **Vendor API docs:** https://docs.snyk.io/snyk-api/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Access Requests](actions/get-access-requests.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snyk/latest/actions/get-access-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (60)

### Access Request

| Action | Method | Description |
| --- | --- | --- |
| [List Access Requests](actions/get-access-requests.md) | GET | Retrieves access requests for the current Snyk user. |

### Api Version

| Action | Method | Description |
| --- | --- | --- |
| [Get API Version](actions/get-api-version.md) | GET | Retrieves an API version specification from Snyk. |
| [List API Versions](actions/list-api-versions.md) | GET | Retrieves available API versions from Snyk. |

### App Bot

| Action | Method | Description |
| --- | --- | --- |
| [List App Bots](actions/get-app-bots.md) | GET | Retrieves app bots from a Snyk organization. |

### App Install

| Action | Method | Description |
| --- | --- | --- |
| [List Group App Installs](actions/get-app-installs-for-group.md) | GET | Retrieves app installs from a Snyk group. |
| [List Organization App Installs](actions/get-app-installs-for-org.md) | GET | Retrieves app installs from a Snyk organization. |
| [List User App Installs](actions/get-app-installs-for-user.md) | GET | Retrieves app installs for the current Snyk user. |

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Get App By Client ID](actions/get-app.md) | GET | Retrieves an app from a Snyk organization by client ID. |
| [Get App By ID](actions/get-app-by-id.md) | GET | Retrieves a created app from a Snyk organization. |
| [List Organization Apps](actions/get-apps.md) | GET | Retrieves apps from a Snyk organization. |
| [List Organization App Creations](actions/get-org-apps.md) | GET | Retrieves created apps from a Snyk organization. |
| [List User Installed Apps](actions/get-user-installed-apps.md) | GET | Retrieves installed apps for the current Snyk user. |

### Asset

| Action | Method | Description |
| --- | --- | --- |
| [Get Asset](actions/get-asset.md) | GET | Retrieves an asset from a Snyk group. |
| [List Group Inventory Assets](actions/list-assets-group.md) | GET | Retrieves inventory assets from a Snyk group. |
| [List Related Assets](actions/list-related-assets.md) | GET | Retrieves related assets from a Snyk asset. |

### Asset Filter Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Group Asset Filter Fields](actions/get-filter-fields-group.md) | GET | Retrieves asset filter fields from a Snyk group. |

### Asset Filter Value

| Action | Method | Description |
| --- | --- | --- |
| [Get Group Asset Filter Values](actions/get-filter-values-group.md) | GET | Retrieves asset filter values from a Snyk group. |

### Asset Group Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Group Asset Group Fields](actions/get-group-fields-group.md) | GET | Retrieves asset group fields from a Snyk group. |

### Audit Log

| Action | Method | Description |
| --- | --- | --- |
| [List Group Audit Logs](actions/list-group-audit-logs.md) | GET | Searches audit logs in a Snyk group. |

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Get Collection](actions/get-collection.md) | GET | Retrieves a collection from a Snyk organization. |
| [List Collections](actions/get-collections.md) | GET | Retrieves collections from a Snyk organization. |

### Custom Base Image

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Base Image](actions/get-custom-base-image.md) | GET | Retrieves a custom base image from Snyk. |
| [List Custom Base Images](actions/get-custom-base-images.md) | GET | Retrieves custom base images from Snyk. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Organization Policy Events](actions/get-org-policy-events.md) | GET | Retrieves policy events from a Snyk organization. |

### Export

| Action | Method | Description |
| --- | --- | --- |
| [Get Group Export](actions/get-group-export.md) | GET | Retrieves an export from a Snyk group. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from the Snyk API. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups available to the current Snyk user. |

### Issue

| Action | Method | Description |
| --- | --- | --- |
| [Get Group Issue](actions/get-group-issue-by-issue-id.md) | GET | Retrieves an issue from a Snyk group. |
| [List Package Issues](actions/get-issues-per-purl.md) | GET | Retrieves package issues from Snyk by package URL. |
| [Get Organization Issue](actions/get-org-issue-by-issue-id.md) | GET | Retrieves an issue from a Snyk organization. |
| [List Group Issues](actions/list-group-issues.md) | GET | Retrieves issues from a Snyk group. |
| [List Organization Issues](actions/list-org-issues.md) | GET | Retrieves issues from a Snyk organization. |

### Membership

| Action | Method | Description |
| --- | --- | --- |
| [List Tenant Memberships](actions/get-tenant-memberships.md) | GET | Retrieves tenant memberships from the Snyk API. |
| [List Group Memberships](actions/list-group-memberships.md) | GET | Retrieves group memberships from the Snyk API. |
| [List Group Organization Memberships](actions/list-group-user-org-memberships.md) | GET | Retrieves group organization memberships for a Snyk user. |
| [List Organization Memberships](actions/list-org-memberships.md) | GET | Retrieves organization memberships from the Snyk API. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-org.md) | GET | Retrieves an organization from the Snyk API. |
| [List Organizations](actions/list-orgs.md) | GET | Retrieves organizations available to the current Snyk user. |
| [List Organizations In Group](actions/list-orgs-in-group.md) | GET | Retrieves organizations from a Snyk group. |

### Personal Access Token

| Action | Method | Description |
| --- | --- | --- |
| [List Personal Access Tokens](actions/list-personal-access-token.md) | GET | Retrieves personal access tokens for the current Snyk user. |

### Policy

| Action | Method | Description |
| --- | --- | --- |
| [List Organization Policies](actions/get-org-policies.md) | GET | Retrieves policies from a Snyk organization. |
| [Get Organization Policy](actions/get-org-policy.md) | GET | Retrieves a policy from a Snyk organization. |
| [List Group Policies](actions/list-group-policies.md) | GET | Retrieves policies from a Snyk group. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Project](actions/get-org-project.md) | GET | Retrieves an organization project from Snyk. |
| [List Collection Projects](actions/get-projects-of-collection.md) | GET | Retrieves projects from a Snyk collection. |
| [List Asset Projects](actions/list-asset-projects.md) | GET | Retrieves projects from a Snyk asset. |
| [List Organization Projects](actions/list-org-projects.md) | GET | Retrieves organization projects from the Snyk API. |

### Service Account

| Action | Method | Description |
| --- | --- | --- |
| [List Group Service Accounts](actions/get-many-group-service-account.md) | GET | Retrieves service accounts from a Snyk group. |
| [List Organization Service Accounts](actions/get-many-org-service-accounts.md) | GET | Retrieves service accounts from a Snyk organization. |
| [Get Group Service Account](actions/get-one-group-service-account.md) | GET | Retrieves a service account from a Snyk group. |
| [Get Organization Service Account](actions/get-one-org-service-account.md) | GET | Retrieves a service account from a Snyk organization. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [List User App Sessions](actions/get-user-app-sessions.md) | GET | Retrieves app sessions for the current Snyk user. |

### Sso Connection

| Action | Method | Description |
| --- | --- | --- |
| [List Group SSO Connections](actions/list-group-sso-connections.md) | GET | Retrieves SSO connections from a Snyk group. |

### Sso User

| Action | Method | Description |
| --- | --- | --- |
| [List Group SSO Connection Users](actions/list-group-sso-connection-users.md) | GET | Retrieves users from a Snyk group SSO connection. |

### Target

| Action | Method | Description |
| --- | --- | --- |
| [Get Target](actions/get-orgs-target.md) | GET | Retrieves a target from a Snyk organization. |
| [List Targets](actions/get-orgs-targets.md) | GET | Retrieves targets from a Snyk organization. |

### Tenant

| Action | Method | Description |
| --- | --- | --- |
| [Get Tenant](actions/get-tenant.md) | GET | Retrieves a tenant from the Snyk API. |
| [List Tenants](actions/list-tenants.md) | GET | Retrieves tenants available to the current Snyk user. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Self](actions/get-self.md) | GET | Retrieves details for the current Snyk user. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from a Snyk organization. |

