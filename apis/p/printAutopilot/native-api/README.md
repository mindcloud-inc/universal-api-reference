# Print Autopilot: Native API Reference

A consolidated summary of Print Autopilot's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/1334461/TW6wJonb
- **API base URL:** `https://printautopilot.com/api`

## Authentication

### Print Autopilot Tokens

Use two Print Autopilot tokens: a Connection Token for printer and print-job actions, and a Create Token for document creation.

### Credentials

- **Connection Token:** `connectionToken` · required · Used for print-job and printer actions such as listing jobs, creating printers, and finishing print jobs.
- **Create Token:** `apiKey` · required · Used for the Create Document action.

[Official authentication documentation](https://documenter.getpostman.com/view/1334461/TW6wJonb)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | `POST /document/create` | [docs](https://documenter.getpostman.com/view/1334461/TW6wJonb#99ca43c2-821e-471f-8530-e562bfbe642b) |
| [Create Printers](actions/create-printers.md) | `POST /printers` | [docs](https://documenter.getpostman.com/view/1334461/TW6wJonb#f3ab1c25-42d7-4be5-8be5-4027b78feffb) |
| [Finish Documents](actions/finish-documents.md) | `POST /finish-print-jobs` | [docs](https://documenter.getpostman.com/view/1334461/TW6wJonb#a8422cc6-d08f-4b47-9e1e-418a6be82a6e) |
| [List Print Jobs](actions/list-print-jobs.md) | `GET /print-jobs` | [docs](https://documenter.getpostman.com/view/1334461/TW6wJonb#387ef982-0730-46fb-a826-340e86ce23a2) |
