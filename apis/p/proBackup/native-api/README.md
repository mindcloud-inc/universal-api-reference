# ProBackup: Native API Reference

A consolidated summary of ProBackup's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://apps.make.com/pro-backup
- **API base URL:** `https://api.probackup.io`

## Authentication

### API Key

API key authentication for the documented ProBackup / Make.com integration surface.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.probackup.io/en/articles/13250944-how-to-connect-make-com-to-probackup)

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Platforms](actions/list-platforms.md) | `GET /backups/v1/platforms` | [docs](https://support.probackup.io/en/articles/13250957-supported-features-for-the-make-com-integration) |
