# Calibre: Native API Reference

A consolidated summary of Calibre's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://calibreapp.com/docs/automation/node
- **API base URL:** `https://api.calibreapp.com`

## Authentication

### Calibre API Token

Use a Calibre API token generated from Account and Billing. This run uses the token-authenticated GraphQL surface.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://calibreapp.com/docs/account-and-billing/manage-api-tokens)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `organisation.sitesList.nodes`.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Deploy](actions/create-deploy.md) | `POST /graphql` | [docs](https://calibreapp.com/docs/automation/deploys#create-deploy) |
| [Create Integration](actions/create-integration.md) | `POST /graphql` | [docs](https://calibreapp.com/docs/automation/integrations#create-integration) |
| [Create Page Test](actions/create-page-test.md) | `POST /graphql` | [docs](https://calibreapp.com/docs/automation/single-page-tests#create-a-page-test) |
| [Create Pull Request Review](actions/create-pull-request-review.md) | `POST /graphql` | [docs](https://calibreapp.com/docs/automation/pull-request-reviews#create-a-pull-request-review) |
| [Create Site](actions/create-site.md) | `POST /graphql` | [docs](https://calibreapp.com/docs/automation/managing-sites#create-a-site) |
| [Create Snapshot](actions/create-snapshot.md) | `POST /graphql` | [docs](https://calibreapp.com/docs/automation/snapshots#create-a-snapshot) |
| [Create Test Profile](actions/create-test-profile.md) | `POST /graphql` | [docs](https://calibreapp.com/docs/automation/test-profiles#create-a-test-profile) |
| [Delete Deploy](actions/delete-deploy.md) | `POST /graphql` | [docs](https://calibreapp.com/docs/automation/deploys#delete-deploy) |
| [Delete Snapshot](actions/delete-snapshot.md) | `POST /graphql` | [docs](https://calibreapp.com/docs/automation/snapshots#delete-a-snapshot) |
| [Download Snapshot Artifacts](actions/download-snapshot-artifacts.md) | `POST /graphql` | [docs](https://calibreapp.com/docs/automation/snapshots#download-snapshot-artifacts) |
| [Download Test Artifacts](actions/download-test-artifacts.md) | `POST /graphql` | [docs](https://calibreapp.com/docs/automation/single-page-tests#retrieve-test-artifacts) |
| [Get Page Test](actions/get-page-test.md) | `POST /graphql` | [docs](https://calibreapp.com/docs/automation/single-page-tests#view-an-existing-test) |
| [Get Pull Request Review](actions/get-pull-request-review.md) | `POST /graphql` | [docs](https://calibreapp.com/docs/automation/pull-request-reviews#view-an-existing-pull-request-review) |
| [Get Snapshot Metrics](actions/get-snapshot-metrics.md) | `POST /graphql` | [docs](https://calibreapp.com/docs/automation/retrieving-metrics#metrics-from-a-single-snapshot) |
| [List Deploys](actions/list-deploys.md) | `POST /graphql` | [docs](https://calibreapp.com/docs/automation/deploys#list-deploys) |
| [List Integrations](actions/list-integrations.md) | `POST /graphql` | [docs](https://calibreapp.com/docs/automation/integrations#list-integrations) |
| [List Page Tests](actions/list-page-tests.md) | `POST /graphql` | [docs](https://calibreapp.com/docs/automation/single-page-tests#list-all-tests) |
| [List Pull Request Reviews](actions/list-pull-request-reviews.md) | `POST /graphql` | [docs](https://calibreapp.com/docs/automation/pull-request-reviews#list-pull-request-reviews) |
| [List Site Metrics](actions/list-site-metrics.md) | `POST /graphql` | [docs](https://calibreapp.com/docs/automation/retrieving-metrics#timeseries-metrics-for-a-given-site) |
| [List Sites](actions/list-sites.md) | `POST /graphql` | [docs](https://calibreapp.com/docs/automation/managing-sites#list-all-sites) |
| [List Snapshots](actions/list-snapshots.md) | `POST /graphql` | [docs](https://calibreapp.com/docs/automation/snapshots#list-snapshots) |
| [List Test Profiles](actions/list-test-profiles.md) | `POST /graphql` | [docs](https://calibreapp.com/docs/automation/test-profiles#list-test-profiles) |
| [Update Integration](actions/update-integration.md) | `POST /graphql` | [docs](https://calibreapp.com/docs/automation/integrations#update-integration) |
| [Update Test Profile](actions/update-test-profile.md) | `POST /graphql` | [docs](https://calibreapp.com/docs/automation/test-profiles#update-a-test-profile) |
