# <img src="https://images.mindcloud.co/apps/icons/intruder_1775591419570.png" alt="Intruder logo" width="28" height="28"> Intruder: Universal API

Manage Intruder targets, scans, and vulnerability issues

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/intruder/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.intruder.io
- **Vendor API docs:** https://developers.intruder.io/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Health](actions/check-health.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intruder/latest/actions/check-health?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Api

| Action | Method | Description |
| --- | --- | --- |
| [Add Target API Schema](actions/add-target-api-schema.md) | POST |  |
| [Update Target API Schema](actions/update-target-api-schema.md) | PUT |  |

### Api Schema

| Action | Method | Description |
| --- | --- | --- |
| [Delete Target API Schema](actions/delete-target-api-schema.md) | DELETE |  |
| [List Target API Schemas](actions/list-target-api-schemas.md) | GET |  |

### Health

| Action | Method | Description |
| --- | --- | --- |
| [Check Health](actions/check-health.md) | GET |  |

### Issue

| Action | Method | Description |
| --- | --- | --- |
| [List Issues](actions/list-issues.md) | GET |  |
| [Snooze Issue](actions/snooze-issue.md) | PUT |  |

### License

| Action | Method | Description |
| --- | --- | --- |
| [List Licenses](actions/list-licenses.md) | GET |  |

### Occurrence

| Action | Method | Description |
| --- | --- | --- |
| [List Issue Occurrences](actions/list-issue-occurrences.md) | GET |  |
| [List Occurrence Scanner Output](actions/list-occurrence-scanner-output.md) | GET |  |
| [Snooze Issue Occurrence](actions/snooze-issue-occurrence.md) | PUT |  |

### Scan

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Scan](actions/cancel-scan.md) | PUT |  |
| [Create Scan Schedule](actions/create-scan-schedule.md) | POST |  |
| [Delete Scan Schedule](actions/delete-scan-schedule.md) | DELETE |  |
| [List Scans](actions/list-scans.md) | GET |  |
| [Retrieve Scan Details](actions/retrieve-scan-details.md) | GET |  |
| [Start Scan](actions/start-scan.md) | POST |  |
| [Update Scan Schedule](actions/update-scan-schedule.md) | PUT |  |

### Scan Schedule

| Action | Method | Description |
| --- | --- | --- |
| [List Scan Schedules](actions/list-scan-schedules.md) | GET |  |

### Target

| Action | Method | Description |
| --- | --- | --- |
| [Add Target](actions/add-target.md) | POST |  |
| [Bulk Add Targets](actions/bulk-add-targets.md) | POST |  |
| [Delete Target](actions/delete-target.md) | DELETE |  |
| [List Targets](actions/list-targets.md) | GET |  |

### Target Authentication

| Action | Method | Description |
| --- | --- | --- |
| [Add Target Authentication](actions/add-target-authentication.md) | POST |  |
| [Delete Target Authentication](actions/delete-target-authentication.md) | DELETE |  |
| [List Target Authentications](actions/list-target-authentications.md) | GET |  |
| [Update Target Authentication](actions/update-target-authentication.md) | PUT |  |

### Target Tag

| Action | Method | Description |
| --- | --- | --- |
| [Delete Target Tag](actions/delete-target-tag.md) | DELETE |  |

