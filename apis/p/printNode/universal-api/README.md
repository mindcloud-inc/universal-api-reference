# <img src="https://images.mindcloud.co/apps/icons/preview-printnode_1773766300342.png" alt="PrintNode logo" width="28" height="28"> PrintNode: Universal API

PrintNode: Manage printers, print jobs, computers, and client downloads

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/printNode/latest
- **Category:** Support / Field Service
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.printnode.com
- **Vendor API docs:** https://www.printnode.com/en/docs/api/curl

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate Credentials](actions/validate-credentials.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printNode/latest/actions/validate-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Builds

| Action | Method | Description |
| --- | --- | --- |
| [Get Latest Client Download](actions/get-latest-client-download.md) | GET | Retrieves the latest client download from PrintNode by operating system. |
| [List Download Clients](actions/list-download-clients.md) | GET | Retrieves available client downloads from PrintNode. |
| [List Download Clients by Set](actions/list-download-clients-by-set.md) | GET | Retrieves specific client downloads from PrintNode by ID set. |
| [Update Download Clients](actions/update-download-clients.md) | PUT | Updates specific client downloads in PrintNode. |

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Delete Computers](actions/delete-computers.md) | DELETE | Deletes one or more computers from PrintNode. |
| [Delete Computers by Set](actions/delete-computers-by-set.md) | DELETE | Deletes specific computers from PrintNode by ID set. |
| [Get Computer Scale](actions/get-computer-scale.md) | GET | Retrieves a specific scale from PrintNode. |
| [Get Computer Scales by Device Name](actions/get-computer-scales-by-device-name.md) | GET | Retrieves scales by device name for a computer from PrintNode. |
| [List Computer Printers](actions/list-computer-printers.md) | GET | Retrieves printers for specific computers from PrintNode. |
| [List Computer Printers by Set](actions/list-computer-printers-by-set.md) | GET | Retrieves specific printers for specific computers from PrintNode. |
| [List Computer Scales](actions/list-computer-scales.md) | GET | Retrieves scales for a specific computer from PrintNode. |
| [List Computers](actions/list-computers.md) | GET | Retrieves all connected computers from PrintNode. |
| [List Computers by Set](actions/list-computers-by-set.md) | GET | Retrieves specific computers from PrintNode by ID set. |
| [List Printers](actions/list-printers.md) | GET | Retrieves all available printers from PrintNode. |
| [List Printers by Set](actions/list-printers-by-set.md) | GET | Retrieves specific printers from PrintNode by ID set. |
| [Simulate Test Scale Measurement](actions/simulate-test-scale-measurement.md) | PUT | Simulates a test scale measurement in PrintNode. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Print Jobs](actions/cancel-print-jobs.md) | DELETE | Cancels undelivered print jobs in PrintNode. |
| [Cancel Print Jobs by Set](actions/cancel-print-jobs-by-set.md) | DELETE | Cancels specific undelivered print jobs in PrintNode. |
| [Cancel Printer Print Jobs](actions/cancel-printer-print-jobs.md) | DELETE | Cancels undelivered print jobs for specific printers in PrintNode. |
| [Cancel Printer Print Jobs by Set](actions/cancel-printer-print-jobs-by-set.md) | DELETE | Cancels specific undelivered print jobs for specific printers in PrintNode. |
| [Create Print Job](actions/create-print-job.md) | POST | Creates a new print job in PrintNode. |
| [List Print Job States](actions/list-print-job-states.md) | GET | Retrieves print job states from PrintNode. |
| [List Print Job States by Set](actions/list-print-job-states-by-set.md) | GET | Retrieves print job states for specific jobs from PrintNode. |
| [List Print Jobs](actions/list-print-jobs.md) | GET | Retrieves print job history from PrintNode. |
| [List Print Jobs by Set](actions/list-print-jobs-by-set.md) | GET | Retrieves specific print jobs from PrintNode by ID set. |
| [List Printer Print Jobs](actions/list-printer-print-jobs.md) | GET | Retrieves print jobs for specific printers from PrintNode. |
| [List Printer Print Jobs by Set](actions/list-printer-print-jobs-by-set.md) | GET | Retrieves specific print jobs for specific printers from PrintNode. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [Ping](actions/ping.md) | GET | Checks the availability of the PrintNode API. |
| [Validate Credentials](actions/validate-credentials.md) | GET | Validates credentials with PrintNode without performing other actions. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Account](actions/get-current-account.md) | GET | Retrieves current account details from PrintNode. |

