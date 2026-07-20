# Buildkite: Native API Reference

A consolidated summary of Buildkite's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://buildkite.com/docs/apis/rest-api
- **API base URL:** `https://api.buildkite.com/v2`

## Authentication

### API Access Token

Buildkite API access token sent as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://buildkite.com/docs/apis/rest-api/access-token)

## Pagination

Use `per_page` in the query string to set the page size (default 25; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Build](actions/cancel-build.md) | `PUT /organizations/:organization/pipelines/:pipeline/builds/:build/cancel` | [docs](https://buildkite.com/docs/apis/rest-api/builds) |
| [Create Annotation](actions/create-annotation.md) | `POST /organizations/:organization/pipelines/:pipeline/builds/:build/annotations` | [docs](https://buildkite.com/docs/apis/rest-api/annotations) |
| [Create Build](actions/create-build.md) | `POST /organizations/:organization/pipelines/:pipeline/builds` | [docs](https://buildkite.com/docs/apis/rest-api/builds) |
| [Delete Annotation](actions/delete-annotation.md) | `DELETE /organizations/:organization/pipelines/:pipeline/builds/:build/annotations/:annotation` | [docs](https://buildkite.com/docs/apis/rest-api/annotations) |
| [Delete Job Log](actions/delete-job-log.md) | `DELETE /organizations/:organization/pipelines/:pipeline/builds/:build/jobs/:job/log` | [docs](https://buildkite.com/docs/apis/rest-api/jobs) |
| [Download Artifact](actions/download-artifact.md) | `GET /organizations/:organization/pipelines/:pipeline/builds/:build/jobs/:job/artifacts/:artifact/download` | [docs](https://buildkite.com/docs/apis/rest-api/artifacts) |
| [Get Build](actions/get-build.md) | `GET /organizations/:organization/pipelines/:pipeline/builds/:build` | [docs](https://buildkite.com/docs/apis/rest-api/builds) |
| [Get Current Access Token](actions/get-current-access-token.md) | `GET /access-token` | [docs](https://buildkite.com/docs/apis/rest-api/access-token) |
| [Get Current User](actions/get-current-user.md) | `GET /user` | [docs](https://buildkite.com/docs/apis/rest-api/user) |
| [Get Job](actions/get-job.md) | `GET /organizations/:organization/pipelines/:pipeline/builds/:build/jobs/:job` | [docs](https://buildkite.com/docs/apis/rest-api/jobs) |
| [Get Job Log](actions/get-job-log.md) | `GET /organizations/:organization/pipelines/:pipeline/builds/:build/jobs/:job/log` | [docs](https://buildkite.com/docs/apis/rest-api/jobs) |
| [Get Organization](actions/get-organization.md) | `GET /organizations/:organization` | [docs](https://buildkite.com/docs/apis/rest-api/organizations) |
| [Get Organization Member](actions/get-organization-member.md) | `GET /organizations/:organization/members/:user` | [docs](https://buildkite.com/docs/apis/rest-api/organizations/members) |
| [Get Pipeline](actions/get-pipeline.md) | `GET /organizations/:organization/pipelines/:pipeline` | [docs](https://buildkite.com/docs/apis/rest-api/pipelines) |
| [Get Team](actions/get-team.md) | `GET /organizations/:organization/teams/:team` | [docs](https://buildkite.com/docs/apis/rest-api/teams) |
| [Get Team Member](actions/get-team-member.md) | `GET /organizations/:organization/teams/:team/members/:user` | [docs](https://buildkite.com/docs/apis/rest-api/teams/members) |
| [Get Team Pipeline](actions/get-team-pipeline.md) | `GET /organizations/:organization/teams/:team/pipelines/:pipeline` | [docs](https://buildkite.com/docs/apis/rest-api/teams/pipelines) |
| [List All Builds](actions/list-all-builds.md) | `GET /builds` | [docs](https://buildkite.com/docs/apis/rest-api/builds) |
| [List Build Annotations](actions/list-build-annotations.md) | `GET /organizations/:organization/pipelines/:pipeline/builds/:build/annotations` | [docs](https://buildkite.com/docs/apis/rest-api/annotations) |
| [List Build Artifacts](actions/list-build-artifacts.md) | `GET /organizations/:organization/pipelines/:pipeline/builds/:build/artifacts` | [docs](https://buildkite.com/docs/apis/rest-api/artifacts) |
| [List Job Artifacts](actions/list-job-artifacts.md) | `GET /organizations/:organization/pipelines/:pipeline/builds/:build/jobs/:job/artifacts` | [docs](https://buildkite.com/docs/apis/rest-api/artifacts) |
| [List Organization Builds](actions/list-organization-builds.md) | `GET /organizations/:organization/builds` | [docs](https://buildkite.com/docs/apis/rest-api/builds) |
| [List Organization Members](actions/list-organization-members.md) | `GET /organizations/:organization/members` | [docs](https://buildkite.com/docs/apis/rest-api/organizations/members) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://buildkite.com/docs/apis/rest-api/organizations) |
| [List Pipeline Builds](actions/list-pipeline-builds.md) | `GET /organizations/:organization/pipelines/:pipeline/builds` | [docs](https://buildkite.com/docs/apis/rest-api/builds) |
| [List Pipelines](actions/list-pipelines.md) | `GET /organizations/:organization/pipelines` | [docs](https://buildkite.com/docs/apis/rest-api/pipelines) |
| [List Team Members](actions/list-team-members.md) | `GET /organizations/:organization/teams/:team/members` | [docs](https://buildkite.com/docs/apis/rest-api/teams/members) |
| [List Team Pipelines](actions/list-team-pipelines.md) | `GET /organizations/:organization/teams/:team/pipelines` | [docs](https://buildkite.com/docs/apis/rest-api/teams/pipelines) |
| [List Teams](actions/list-teams.md) | `GET /organizations/:organization/teams` | [docs](https://buildkite.com/docs/apis/rest-api/teams) |
| [Rebuild Build](actions/rebuild-build.md) | `PUT /organizations/:organization/pipelines/:pipeline/builds/:build/rebuild` | [docs](https://buildkite.com/docs/apis/rest-api/builds) |
| [Reprioritize Job](actions/reprioritize-job.md) | `PUT /organizations/:organization/pipelines/:pipeline/builds/:build/jobs/:job/reprioritize` | [docs](https://buildkite.com/docs/apis/rest-api/jobs) |
| [Retry Job](actions/retry-job.md) | `PUT /organizations/:organization/pipelines/:pipeline/builds/:build/jobs/:job/retry` | [docs](https://buildkite.com/docs/apis/rest-api/jobs) |
| [Revoke Current Access Token](actions/revoke-current-access-token.md) | `DELETE /access-token` | [docs](https://buildkite.com/docs/apis/rest-api/access-token) |
| [Unblock Job](actions/unblock-job.md) | `PUT /organizations/:organization/pipelines/:pipeline/builds/:build/jobs/:job/unblock` | [docs](https://buildkite.com/docs/apis/rest-api/jobs) |
