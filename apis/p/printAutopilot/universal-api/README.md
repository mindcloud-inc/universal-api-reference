# <img src="https://images.mindcloud.co/apps/icons/print-autopilot_1774554188635.png" alt="Print Autopilot logo" width="28" height="28"> Print Autopilot: Universal API

Queue documents, manage printers, and track print jobs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/printAutopilot/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://printautopilot.com
- **Vendor API docs:** https://documenter.getpostman.com/view/1334461/TW6wJonb

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Print Jobs](actions/list-print-jobs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printAutopilot/latest/actions/list-print-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Create Printers](actions/create-printers.md) | POST | Creates printers in Print Autopilot. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST | Creates a document in Print Autopilot from a base64 PDF. |
| [Finish Documents](actions/finish-documents.md) | PUT | Updates document statuses in Print Autopilot. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [List Print Jobs](actions/list-print-jobs.md) | GET | Retrieves print jobs from Print Autopilot. |

