# ClassDo: Native API Reference

A consolidated summary of ClassDo's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://developer.classdo.com/schema/
- **API base URL:** `https://api.classdo.com`

## Authentication

### API Key

ClassDo GraphQL API key authentication via x-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://developer.classdo.com/api/graphql/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Room Members](actions/add-room-members.md) | `POST /graphql` | [docs](https://developer.classdo.com/schema/mutation.doc) |
| [Create Room](actions/create-room.md) | `POST /graphql` | [docs](https://developer.classdo.com/schema/mutation.doc) |
| [Delete Room](actions/delete-room.md) | `POST /graphql` | [docs](https://developer.classdo.com/schema/mutation.doc) |
| [Delete Room Member](actions/delete-room-member.md) | `POST /graphql` | [docs](https://developer.classdo.com/schema/mutation.doc) |
| [Get Viewer](actions/get-viewer.md) | `POST /graphql` | [docs](https://developer.classdo.com/schema/viewer.doc) |
| [List Organization Member Roles](actions/list-organization-member-roles.md) | `POST /graphql` | [docs](https://developer.classdo.com/schema/viewer.doc) |
| [List Organization Members](actions/list-organization-members.md) | `POST /graphql` | [docs](https://developer.classdo.com/schema/viewer.doc) |
| [List Rooms](actions/list-rooms.md) | `POST /graphql` | [docs](https://developer.classdo.com/schema/viewer.doc) |
| [Lock Room](actions/lock-room.md) | `POST /graphql` | [docs](https://developer.classdo.com/schema/mutation.doc) |
| [Search Recording Videos](actions/search-recording-videos.md) | `POST /graphql` | [docs](https://developer.classdo.com/schema/viewer.doc) |
| [Send Invitation](actions/send-invitation.md) | `POST /graphql` | [docs](https://developer.classdo.com/schema/mutation.doc) |
| [Start Recording](actions/start-recording.md) | `POST /graphql` | [docs](https://developer.classdo.com/schema/mutation.doc) |
| [Stop Recording](actions/stop-recording.md) | `POST /graphql` | [docs](https://developer.classdo.com/schema/mutation.doc) |
| [Unlock Room](actions/unlock-room.md) | `POST /graphql` | [docs](https://developer.classdo.com/schema/mutation.doc) |
| [Update Organization Member](actions/update-organization-member.md) | `POST /graphql` | [docs](https://developer.classdo.com/schema/mutation.doc) |
