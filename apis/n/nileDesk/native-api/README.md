# NileDesk: Native API Reference

A consolidated summary of NileDesk's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://niledesk.com/api
- **API base URL:** `https://app.niledesk.com/api/public`

## Authentication

### API Key + Org ID

Connect NileDesk with your personal API key and organization ID.

### Credentials

- **API Key:** `apiKey` · required
- **Organization ID:** `orgId` · required · Your NileDesk organization ID, which is the same value you use to sign in.

Send these headers with each API request:

```http
X-Org-Id: <orgId>
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://niledesk.com/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Record](actions/add-record.md) | `POST /AddRecord` | [docs](https://niledesk.com/api) |
| [Approve Item](actions/approve-item.md) | `POST /ApproveItem` | [docs](https://niledesk.com/api) |
| [Count Records](actions/count-records.md) | `POST /CountRecords` | [docs](https://niledesk.com/api) |
| [Create Board Item](actions/create-board-item.md) | `POST /InitiateBoardItem` | [docs](https://niledesk.com/api) |
| [Create Draft Board Item](actions/create-draft-board-item.md) | `POST /CreateBoardDraftItem` | [docs](https://niledesk.com/api) |
| [Create Draft Process Flow Item](actions/create-draft-process-flow-item.md) | `POST /CreateProcessDraftItem` | [docs](https://niledesk.com/api) |
| [Create Process Flow Item](actions/create-process-flow-item.md) | `POST /InitiateProcessItem` | [docs](https://niledesk.com/api) |
| [Delete Many Records](actions/delete-many-records.md) | `POST /DeleteManyRecords` | [docs](https://niledesk.com/api) |
| [Delete One Record](actions/delete-one-record.md) | `POST /DeleteOneRecord` | [docs](https://niledesk.com/api) |
| [Find Many Records](actions/find-many-records.md) | `POST /FindManyRecord` | [docs](https://niledesk.com/api) |
| [Find One Record](actions/find-one-record.md) | `POST /FindOneRecord` | [docs](https://niledesk.com/api) |
| [Get Process Timeline](actions/get-process-timeline.md) | `POST /GetProcessTimeline` | [docs](https://niledesk.com/api) |
| [List Template Fields](actions/list-template-fields.md) | `POST /GetFields` | [docs](https://niledesk.com/api) |
| [List Templates](actions/list-templates.md) | `POST /GetTemplates` | [docs](https://niledesk.com/api) |
| [Move Board Item To Step](actions/move-board-item-to-step.md) | `POST /SwitchBoardStep` | [docs](https://niledesk.com/api) |
| [Reject Item](actions/reject-item.md) | `POST /RejectItem` | [docs](https://niledesk.com/api) |
| [Return Item To Last Executed Step](actions/return-item-to-last-executed-step.md) | `POST /ReturnItemToLastExecutedStep` | [docs](https://niledesk.com/api) |
| [Send Process Item Forward](actions/send-process-item-forward.md) | `POST /ProcessItem` | [docs](https://niledesk.com/api) |
| [Update Many Records](actions/update-many-records.md) | `POST /UpdateManyRecords` | [docs](https://niledesk.com/api) |
| [Update One Record](actions/update-one-record.md) | `POST /UpdateOneRecord` | [docs](https://niledesk.com/api) |
