# PrintNode: Native API Reference

A consolidated summary of PrintNode's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://www.printnode.com/en/docs/api/curl
- **API base URL:** `https://api.printnode.com`

## Authentication

### API Key (Basic Auth)

Use your PrintNode API key as the username and leave the password blank.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://www.printnode.com/en/docs/api/curl#get-whoami)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Print Jobs](actions/cancel-print-jobs.md) | `DELETE /printjobs` | [docs](https://www.printnode.com/en/docs/api/curl#printjobs-removing) |
| [Cancel Print Jobs by Set](actions/cancel-print-jobs-by-set.md) | `DELETE /printjobs/:printJobSet` | [docs](https://www.printnode.com/en/docs/api/curl#printjobs-removing) |
| [Cancel Printer Print Jobs](actions/cancel-printer-print-jobs.md) | `DELETE /printers/:printerSet/printjobs` | [docs](https://www.printnode.com/en/docs/api/curl#printjobs-removing) |
| [Cancel Printer Print Jobs by Set](actions/cancel-printer-print-jobs-by-set.md) | `DELETE /printers/:printerSet/printjobs/:printJobSet` | [docs](https://www.printnode.com/en/docs/api/curl#printjobs-removing) |
| [Create Print Job](actions/create-print-job.md) | `POST /printjobs` | [docs](https://www.printnode.com/en/docs/api/curl#printjob-creating) |
| [Delete Computers](actions/delete-computers.md) | `DELETE /computers` | [docs](https://www.printnode.com/en/docs/api/curl#computers-removing) |
| [Delete Computers by Set](actions/delete-computers-by-set.md) | `DELETE /computers/:computerSet` | [docs](https://www.printnode.com/en/docs/api/curl#computers-removing) |
| [Get Computer Scale](actions/get-computer-scale.md) | `GET /computer/:computerId/scale/:deviceName/:deviceNumber` | [docs](https://www.printnode.com/en/docs/api/curl#scales-http) |
| [Get Computer Scales by Device Name](actions/get-computer-scales-by-device-name.md) | `GET /computer/:computerId/scales/:deviceName` | [docs](https://www.printnode.com/en/docs/api/curl#scales-http) |
| [Get Current Account](actions/get-current-account.md) | `GET /whoami` | [docs](https://www.printnode.com/en/docs/api/curl#whoami) |
| [Get Latest Client Download](actions/get-latest-client-download.md) | `GET /download/client/:operatingSystem` | [docs](https://www.printnode.com/en/docs/api/curl#account-download-management) |
| [List Computer Printers](actions/list-computer-printers.md) | `GET /computers/:computerSet/printers` | [docs](https://www.printnode.com/en/docs/api/curl#printers-viewing) |
| [List Computer Printers by Set](actions/list-computer-printers-by-set.md) | `GET /computers/:computerSet/printers/:printerSet` | [docs](https://www.printnode.com/en/docs/api/curl#printers-viewing) |
| [List Computer Scales](actions/list-computer-scales.md) | `GET /computer/:computerId/scales` | [docs](https://www.printnode.com/en/docs/api/curl#scales-http) |
| [List Computers](actions/list-computers.md) | `GET /computers` | [docs](https://www.printnode.com/en/docs/api/curl#computers-viewing) |
| [List Computers by Set](actions/list-computers-by-set.md) | `GET /computers/:computerSet` | [docs](https://www.printnode.com/en/docs/api/curl#computers-viewing) |
| [List Download Clients](actions/list-download-clients.md) | `GET /download/clients` | [docs](https://www.printnode.com/en/docs/api/curl#account-download-management) |
| [List Download Clients by Set](actions/list-download-clients-by-set.md) | `GET /download/clients/:downloadSet` | [docs](https://www.printnode.com/en/docs/api/curl#account-download-management) |
| [List Print Job States](actions/list-print-job-states.md) | `GET /printjobs/states` | [docs](https://www.printnode.com/en/docs/api/curl#printjob-states) |
| [List Print Job States by Set](actions/list-print-job-states-by-set.md) | `GET /printjobs/:printJobSet/states` | [docs](https://www.printnode.com/en/docs/api/curl#printjob-states) |
| [List Print Jobs](actions/list-print-jobs.md) | `GET /printjobs` | [docs](https://www.printnode.com/en/docs/api/curl#printjob-viewing) |
| [List Print Jobs by Set](actions/list-print-jobs-by-set.md) | `GET /printjobs/:printJobSet` | [docs](https://www.printnode.com/en/docs/api/curl#printjob-viewing) |
| [List Printer Print Jobs](actions/list-printer-print-jobs.md) | `GET /printers/:printerSet/printjobs` | [docs](https://www.printnode.com/en/docs/api/curl#printjob-viewing) |
| [List Printer Print Jobs by Set](actions/list-printer-print-jobs-by-set.md) | `GET /printers/:printerSet/printjobs/:printJobSet` | [docs](https://www.printnode.com/en/docs/api/curl#printjob-viewing) |
| [List Printers](actions/list-printers.md) | `GET /printers` | [docs](https://www.printnode.com/en/docs/api/curl#printers-viewing) |
| [List Printers by Set](actions/list-printers-by-set.md) | `GET /printers/:printerSet` | [docs](https://www.printnode.com/en/docs/api/curl#printers-viewing) |
| [Ping](actions/ping.md) | `GET /ping` | [docs](https://www.printnode.com/en/docs/api/curl#misc-ping) |
| [Simulate Test Scale Measurement](actions/simulate-test-scale-measurement.md) | `PUT /scale` | [docs](https://www.printnode.com/en/docs/api/curl#scales-testing) |
| [Update Download Clients](actions/update-download-clients.md) | `PATCH /download/clients/:downloadSet` | [docs](https://www.printnode.com/en/docs/api/curl#account-download-management) |
| [Validate Credentials](actions/validate-credentials.md) | `GET /noop` | [docs](https://www.printnode.com/en/docs/api/curl#misc-noop) |
