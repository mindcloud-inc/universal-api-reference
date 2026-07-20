# Sentry IO: Native API Reference

A consolidated summary of Sentry IO's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://docs.sentry.io/api/
- **API base URL:** `https://sentry.io/api/0`

## Authentication

### Sentry OAuth2

Connect to Sentry using OAuth2 authorization code flow.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://sentry.io/oauth/authorize/ to approve access.
2. Exchange the returned authorization code with a POST request to https://sentry.io/oauth/token/.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `org:read project:read team:read member:read event:read event:write project:releases`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://sentry.io/oauth/token/.

[Official authentication documentation](https://docs.sentry.io/api/auth/)

## API conventions

Responses from this API use JSON.

## Pagination

Use `cursor` in the query string as the pagination cursor.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Issue Events](actions/list-issue-events.md) | `GET /organizations/:organization_id_or_slug/issues/:issue_id/events/` | [docs](https://docs.sentry.io/api/events/list-an-issues-events/) |
| [List Organization Issues](actions/list-organization-issues.md) | `GET /organizations/:organization_id_or_slug/issues/` | [docs](https://docs.sentry.io/api/events/list-an-organizations-issues/) |
| [List Organization Members](actions/list-organization-members.md) | `GET /organizations/:organization_id_or_slug/members/` | [docs](https://docs.sentry.io/api/organizations/list-an-organizations-members/) |
| [List Organization Projects](actions/list-organization-projects.md) | `GET /organizations/:organization_id_or_slug/projects/` | [docs](https://docs.sentry.io/api/organizations/list-an-organizations-projects/) |
| [List Organization Releases](actions/list-organization-releases.md) | `GET /organizations/:organization_id_or_slug/releases/` | [docs](https://docs.sentry.io/api/releases/list-an-organizations-releases/) |
| [List Organization Teams](actions/list-organization-teams.md) | `GET /organizations/:organization_id_or_slug/teams/` | [docs](https://docs.sentry.io/api/teams/list-an-organizations-teams/) |
| [List Project Error Events](actions/list-project-error-events.md) | `GET /projects/:organization_id_or_slug/:project_id_or_slug/events/` | [docs](https://docs.sentry.io/api/events/list-a-projects-error-events/) |
| [List Project Users](actions/list-project-users.md) | `GET /projects/:organization_id_or_slug/:project_id_or_slug/users/` | [docs](https://docs.sentry.io/api/projects/list-a-projects-users/) |
| [List Team Members](actions/list-team-members.md) | `GET /teams/:organization_id_or_slug/:team_id_or_slug/members/` | [docs](https://docs.sentry.io/api/teams/list-a-teams-members/) |
| [List Your Organizations](actions/list-your-organizations.md) | `GET /organizations/` | [docs](https://docs.sentry.io/api/users/list-your-organizations/) |
| [Query Explore Events](actions/query-explore-events.md) | `GET /organizations/:organization_id_or_slug/events/` | [docs](https://docs.sentry.io/api/explore/query-explore-events-in-table-format/) |
| [Resolve Event ID](actions/resolve-event-id.md) | `GET /organizations/:organization_id_or_slug/eventids/:event_id/` | [docs](https://docs.sentry.io/api/organizations/resolve-an-event-id/) |
| [Resolve Short ID](actions/resolve-short-id.md) | `GET /organizations/:organization_id_or_slug/shortids/:issue_id/` | [docs](https://docs.sentry.io/api/organizations/resolve-a-short-id/) |
| [Retrieve Issue](actions/retrieve-issue.md) | `GET /organizations/:organization_id_or_slug/issues/:issue_id/` | [docs](https://docs.sentry.io/api/events/retrieve-an-issue/) |
| [Retrieve Issue Event](actions/retrieve-issue-event.md) | `GET /organizations/:organization_id_or_slug/issues/:issue_id/events/:event_id/` | [docs](https://docs.sentry.io/api/events/retrieve-an-issue-event/) |
| [Retrieve Organization](actions/retrieve-organization.md) | `GET /organizations/:organization_id_or_slug/` | [docs](https://docs.sentry.io/api/organizations/retrieve-an-organization/) |
| [Retrieve Organization Member](actions/retrieve-organization-member.md) | `GET /organizations/:organization_id_or_slug/members/:member_id/` | [docs](https://docs.sentry.io/api/organizations/retrieve-an-organization-member/) |
| [Retrieve Organization Release](actions/retrieve-organization-release.md) | `GET /organizations/:organization_id_or_slug/releases/:version/` | [docs](https://docs.sentry.io/api/releases/retrieve-an-organizations-release/) |
| [Retrieve Project](actions/retrieve-project.md) | `GET /projects/:organization_id_or_slug/:project_id_or_slug/` | [docs](https://docs.sentry.io/api/projects/retrieve-a-project/) |
| [Retrieve Project Event Counts](actions/retrieve-project-event-counts.md) | `GET /projects/:organization_id_or_slug/:project_id_or_slug/stats/` | [docs](https://docs.sentry.io/api/projects/retrieve-event-counts-for-a-project/) |
| [Retrieve Team](actions/retrieve-team.md) | `GET /teams/:organization_id_or_slug/:team_id_or_slug/` | [docs](https://docs.sentry.io/api/teams/retrieve-a-team/) |
| [Update Issue](actions/update-issue.md) | `PUT /organizations/:organization_id_or_slug/issues/:issue_id/` | [docs](https://docs.sentry.io/api/events/update-an-issue/) |
