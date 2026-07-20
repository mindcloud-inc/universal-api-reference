# <img src="https://images.mindcloud.co/apps/icons/calibre_1774231388381.png" alt="Calibre logo" width="28" height="28"> Calibre: Universal API

Calibre helps teams monitor website performance, automate snapshots and deployments, and run performance tests across sites and preview environments.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/calibre/latest
- **Category:** IT Operations / Observability
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://calibreapp.com/
- **Vendor API docs:** https://calibreapp.com/docs/automation/node

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sites](actions/list-sites.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calibre/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Deploy

| Action | Method | Description |
| --- | --- | --- |
| [Create Deploy](actions/create-deploy.md) | POST | Creates a new deploy in Calibre. |
| [Delete Deploy](actions/delete-deploy.md) | DELETE | Deletes an existing deploy from Calibre. |
| [List Deploys](actions/list-deploys.md) | GET | Retrieves deploys for a site from Calibre. |

### Integration

| Action | Method | Description |
| --- | --- | --- |
| [Create Integration](actions/create-integration.md) | POST | Creates a new integration in Calibre. |
| [List Integrations](actions/list-integrations.md) | GET | Retrieves integrations for a site from Calibre. |
| [Update Integration](actions/update-integration.md) | PUT | Updates an existing integration in Calibre. |

### Metric

| Action | Method | Description |
| --- | --- | --- |
| [List Site Metrics](actions/list-site-metrics.md) | GET | Retrieves timeseries metrics for a site from Calibre. |

### Page Test

| Action | Method | Description |
| --- | --- | --- |
| [Create Page Test](actions/create-page-test.md) | POST | Creates a new page test in Calibre. |
| [Download Test Artifacts](actions/download-test-artifacts.md) | GET | Retrieves artifact download URLs for a page test from Calibre. |
| [Get Page Test](actions/get-page-test.md) | GET | Retrieves a page test by UUID from Calibre. |
| [List Page Tests](actions/list-page-tests.md) | GET | Retrieves page tests for a site from Calibre. |

### Pull Request Review

| Action | Method | Description |
| --- | --- | --- |
| [Create Pull Request Review](actions/create-pull-request-review.md) | POST | Creates a new pull request review in Calibre. |
| [Get Pull Request Review](actions/get-pull-request-review.md) | GET | Retrieves a pull request review by branch from Calibre. |
| [List Pull Request Reviews](actions/list-pull-request-reviews.md) | GET | Retrieves pull request reviews from Calibre. |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [Create Site](actions/create-site.md) | POST | Creates a new site in Calibre. |
| [List Sites](actions/list-sites.md) | GET | Retrieves all available sites from Calibre. |

### Snapshot

| Action | Method | Description |
| --- | --- | --- |
| [Create Snapshot](actions/create-snapshot.md) | POST | Creates a new snapshot for a site in Calibre. |
| [Delete Snapshot](actions/delete-snapshot.md) | DELETE | Deletes an existing snapshot from Calibre. |
| [Download Snapshot Artifacts](actions/download-snapshot-artifacts.md) | GET | Retrieves artifact download URLs for a snapshot from Calibre. |
| [Get Snapshot Metrics](actions/get-snapshot-metrics.md) | GET | Retrieves metrics for a single snapshot from Calibre. |
| [List Snapshots](actions/list-snapshots.md) | GET | Retrieves snapshots for a site from Calibre. |

### Testprofile

| Action | Method | Description |
| --- | --- | --- |
| [Create Test Profile](actions/create-test-profile.md) | POST | Creates a new test profile in Calibre. |
| [List Test Profiles](actions/list-test-profiles.md) | GET | Retrieves test profiles for a site from Calibre. |
| [Update Test Profile](actions/update-test-profile.md) | PUT | Updates an existing test profile in Calibre. |

