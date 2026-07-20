# Push by Techulus: Native API Reference

A consolidated summary of Push by Techulus's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://docs.push.techulus.com/
- **API base URL:** `https://push.techulus.com`

## Authentication

### API Key

Authenticate to Push by Techulus using an account or team API key sent in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.push.techulus.com/api-documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Invite or Team Member](actions/delete-invite-or-team-member.md) | `DELETE /api/management/v1/teams/invite` | [docs](https://docs.push.techulus.com/management-api-beta) |
| [Invite User to Team](actions/invite-user-to-team.md) | `POST /api/management/v1/teams/invite` | [docs](https://docs.push.techulus.com/management-api-beta) |
| [Send Notification](actions/send-notification.md) | `POST /api/v1/notify` | [docs](https://docs.push.techulus.com/api-documentation) |
| [Send Notification Async](actions/send-notification-async.md) | `POST /api/v1/notify-async` | [docs](https://docs.push.techulus.com/api-documentation) |
| [Send Notification to Device Group](actions/send-notification-to-device-group.md) | `POST /api/v1/notify/group/:groupId` | [docs](https://docs.push.techulus.com/api-documentation-1) |
| [Send Notification via GET](actions/send-notification-via-get.md) | `GET /api/v1/notify/:apiKey` | [docs](https://docs.push.techulus.com/api-documentation) |
| [Send Notification via Path API Key](actions/send-notification-via-path-api-key.md) | `POST /api/v1/notify/:apiKey` | [docs](https://docs.push.techulus.com/api-documentation) |
