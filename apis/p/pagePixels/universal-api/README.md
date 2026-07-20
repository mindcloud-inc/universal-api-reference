# <img src="https://images.mindcloud.co/apps/icons/page-pixels_1773843857349.png" alt="PagePixels logo" width="28" height="28"> PagePixels: Universal API

Capture, schedule, and analyze website screenshots and domain data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pagePixels/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pagepixels.com
- **Vendor API docs:** https://pagepixels.com/app/screenshots-api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Limits](actions/get-account-limits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/get-account-limits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Account Limit

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Limits](actions/get-account-limits.md) | GET |  |

### Change Notification

| Action | Method | Description |
| --- | --- | --- |
| [List All Change Notifications](actions/list-all-change-notifications.md) | GET |  |
| [List Change Notifications](actions/list-change-notifications.md) | GET |  |

### Real Location

| Action | Method | Description |
| --- | --- | --- |
| [List Real Locations](actions/list-real-locations.md) | GET |  |

### Screenshot

| Action | Method | Description |
| --- | --- | --- |
| [Capture Screenshot](actions/capture-screenshot.md) | GET |  |
| [Get Screenshots From Configuration](actions/get-screenshots-from-configuration.md) | GET |  |
| [List All Screenshots](actions/list-all-screenshots.md) | GET |  |

### Screenshot Capture

| Action | Method | Description |
| --- | --- | --- |
| [Capture Next Scheduled Screenshot](actions/capture-next-scheduled-screenshot.md) | POST |  |

### Screenshot Configuration

| Action | Method | Description |
| --- | --- | --- |
| [Create Scheduled Screenshot](actions/create-scheduled-screenshot.md) | POST |  |
| [Delete Screenshot Configuration](actions/delete-screenshot-configuration.md) | DELETE |  |
| [Get Screenshot Configuration](actions/get-screenshot-configuration.md) | GET |  |
| [List Screenshot Configurations](actions/list-screenshot-configurations.md) | GET |  |

### Screenshot Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Status](actions/get-job-status.md) | GET |  |

### Website Domain Research Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Website Domain Research Report](actions/get-website-domain-research-report.md) | GET |  |

### Website Domain Research Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Website Domain Research Request](actions/create-website-domain-research-request.md) | POST |  |
| [Get Website Domain Research Job Status](actions/get-website-domain-research-job-status.md) | GET |  |
| [List All Website Domain Research Reports](actions/list-all-website-domain-research-reports.md) | GET |  |

