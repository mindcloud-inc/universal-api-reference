# <img src="https://images.mindcloud.co/apps/icons/lobstr-icon_1776878807798.png" alt="LOBSTR.IO logo" width="28" height="28"> LOBSTR.IO: Universal API

Configure crawlers, launch scraping runs, and collect structured results

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lOBSTRIO/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.lobstr.io
- **Vendor API docs:** https://docs.lobstr.io

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Crawlers](actions/list-crawlers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/list-crawlers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Check Sync Status](actions/check-sync-status.md) | GET | Retrieves sync task status from LOBSTR.IO. |
| [Get Account Details](actions/get-account-details.md) | GET | Retrieves account details from LOBSTR.IO. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accounts from LOBSTR.IO. |
| [Refresh Cookies](actions/refresh-cookies.md) | PUT | Refreshes account cookies in LOBSTR.IO. |
| [Sync Account](actions/sync-account.md) | POST | Synchronizes an account in LOBSTR.IO using cookies. |

### Data Sources

| Action | Method | Description |
| --- | --- | --- |
| [Get Crawler Attributes](actions/get-crawler-attributes.md) | GET | Retrieves crawler attributes from LOBSTR.IO. |
| [Get Crawler Details](actions/get-crawler-details.md) | GET | Retrieves crawler details from LOBSTR.IO. |
| [Get Crawler Parameters](actions/get-crawler-parameters.md) | GET | Retrieves crawler parameters from LOBSTR.IO. |
| [List Crawlers](actions/list-crawlers.md) | GET | Retrieves crawlers from LOBSTR.IO. |

### Data Syncs

| Action | Method | Description |
| --- | --- | --- |
| [Create Squid](actions/create-squid.md) | POST | Creates a new squid in LOBSTR.IO. |
| [Delete Squid](actions/delete-squid.md) | DELETE | Deletes an existing squid from LOBSTR.IO. |
| [Get Squid Details](actions/get-squid-details.md) | GET | Retrieves squid details from LOBSTR.IO. |
| [List Squids](actions/list-squids.md) | GET | Retrieves squids from LOBSTR.IO. |
| [Update Squid](actions/update-squid.md) | PUT | Updates an existing squid in LOBSTR.IO. |

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [Get Results](actions/get-results.md) | GET | Retrieves results from LOBSTR.IO. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Add Tasks](actions/add-tasks.md) | POST | Creates new tasks in LOBSTR.IO. |
| [Check Upload Status](actions/check-upload-status.md) | GET | Retrieves upload task status from LOBSTR.IO. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from LOBSTR.IO. |
| [Upload Tasks](actions/upload-tasks.md) | POST | Uploads tasks to LOBSTR.IO from a file. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get User Profile](actions/get-user-profile.md) | GET | Retrieves your user profile from LOBSTR.IO. |

### Workflow Runs

| Action | Method | Description |
| --- | --- | --- |
| [Get Run](actions/get-run.md) | GET | Retrieves a run from LOBSTR.IO. |
| [Get Run Stats](actions/get-run-stats.md) | GET | Retrieves run stats from LOBSTR.IO. |
| [List Runs](actions/list-runs.md) | GET | Retrieves runs from LOBSTR.IO. |
| [Start Run](actions/start-run.md) | POST | Starts a new run in LOBSTR.IO. |

