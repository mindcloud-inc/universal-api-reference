# <img src="https://images.mindcloud.co/apps/icons/call-scaler_1776881100120.png" alt="CallScaler logo" width="28" height="28"> CallScaler: Universal API

Track, route, and analyze phone calls

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/callScaler/latest
- **Category:** Support / Contact Center
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://callscaler.com
- **Vendor API docs:** https://callscaler.com/docs/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Calls](actions/list-calls.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/list-calls?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Calls

| Action | Method | Description |
| --- | --- | --- |
| [Batch Lookup Calls](actions/batch-lookup-calls.md) | GET | Finds calls in CallScaler by batch lookup. |
| [Get Call](actions/get-call.md) | GET | Retrieves a call from CallScaler. |
| [Get Call Transcription](actions/get-call-transcription.md) | GET | Retrieves a call transcription from CallScaler. |
| [List Calls](actions/list-calls.md) | GET | Retrieves calls from CallScaler. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Export Calls CSV](actions/export-calls-csv.md) | GET | Downloads a calls CSV export from CallScaler. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Add Number Group Members](actions/add-number-group-members.md) | PUT | Updates a number group in CallScaler by adding members. |
| [Create Number Group](actions/create-number-group.md) | POST | Creates a number group in CallScaler. |
| [Delete Number Group](actions/delete-number-group.md) | DELETE | Deletes a number group from CallScaler. |
| [List Number Groups](actions/list-number-groups.md) | GET | Retrieves number groups from CallScaler. |
| [Remove Number Group Member](actions/remove-number-group-member.md) | DELETE | Deletes a number group member from CallScaler. |
| [Update Number Group](actions/update-number-group.md) | PUT | Updates a number group in CallScaler. |

### Phone Numbers

| Action | Method | Description |
| --- | --- | --- |
| [Create Number Pool](actions/create-number-pool.md) | POST | Creates a number pool in CallScaler. |
| [Get Number](actions/get-number.md) | GET |  |
| [Get Number Pool](actions/get-number-pool.md) | GET | Retrieves a number pool from CallScaler. |
| [List Number Group Members](actions/list-number-group-members.md) | GET | Retrieves number group members from CallScaler. |
| [List Number Pools](actions/list-number-pools.md) | GET | Retrieves number pools from CallScaler. |
| [List Numbers](actions/list-numbers.md) | GET | Retrieves numbers from CallScaler. |
| [Purchase Number](actions/purchase-number.md) | POST | Creates a purchased number in CallScaler. |
| [Release Number](actions/release-number.md) | DELETE | Deletes a number from CallScaler. |
| [Search Available Numbers](actions/search-available-numbers.md) | GET | Finds available numbers in CallScaler. |
| [Update Number](actions/update-number.md) | PUT | Updates a number in CallScaler. |

### Recordings

| Action | Method | Description |
| --- | --- | --- |
| [Download Call Recording](actions/download-call-recording.md) | GET | Downloads a call recording from CallScaler. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Call Analytics](actions/get-call-analytics.md) | GET | Retrieves call analytics from CallScaler. |
| [Get Number Group Bulk Stats](actions/get-number-group-bulk-stats.md) | GET | Retrieves number group bulk stats from CallScaler. |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [Create Call Flow](actions/create-call-flow.md) | POST | Creates a call flow in CallScaler. |
| [Delete Call Flow](actions/delete-call-flow.md) | DELETE | Deletes a call flow from CallScaler. |
| [Get Call Flow](actions/get-call-flow.md) | GET | Retrieves a call flow from CallScaler. |
| [List Call Flow Versions](actions/list-call-flow-versions.md) | GET | Retrieves call flow versions from CallScaler. |
| [List Call Flows](actions/list-call-flows.md) | GET | Retrieves call flows from CallScaler. |
| [Update Call Flow](actions/update-call-flow.md) | PUT | Updates a call flow in CallScaler. |

