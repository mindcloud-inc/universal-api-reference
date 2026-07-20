# Jottacloud: Native API Reference

A consolidated summary of Jottacloud's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://docs.jottacloud.com/en/collections/178055-our-command-line-tool
- **API base URL:** `https://api.jotta.cloud`

## Authentication

### Jottacloud Personal Login Token

Authenticate Jottacloud by pasting the single-use Personal Login Token from Jottacloud account security. MindCloud exchanges it into a durable access and refresh session behind the scenes.

### Credentials

- **Personal Login Token:** `personalLoginToken` · required · Paste the single-use Personal Login Token generated from Jottacloud account security settings. MindCloud exchanges it into a durable Jottacloud session.

Send these headers with each API request:

```http
Authorization: Bearer <custom.access_token>
```

[Official authentication documentation](https://docs.jottacloud.com/en/articles/1437248-login-and-basic-use-with-jottacloud-cli)

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Copy Path](actions/copy-path.md) | `POST /files/v2/copy` |  |
| [Create Folder](actions/create-folder.md) | `POST /files/v2/create_folder` |  |
| [Delete Path](actions/delete-path.md) | `POST /files/v2/delete` |  |
| [Disable Public Share](actions/disable-public-share.md) | `POST /shares/v2/public_disable` |  |
| [Enable Public Share](actions/enable-public-share.md) | `POST /shares/v2/public_enable` |  |
| [Get Account Root](actions/get-account-root.md) | `GET https://jfs.jottacloud.com/jfs/{{username}}` |  |
| [Get Archive Mount](actions/get-archive-mount.md) | `GET https://jfs.jottacloud.com/jfs/{{username}}/Jotta/Archive` |  |
| [Get Jotta Device Root](actions/get-jotta-device-root.md) | `GET https://jfs.jottacloud.com/jfs/{{username}}/Jotta` |  |
| [Get Path](actions/get-path.md) | `POST /files/v2/get_path` |  |
| [Get Share Info](actions/get-share-info.md) | `POST /shares/v2/share_info` |  |
| [Get Sync Mount](actions/get-sync-mount.md) | `GET https://jfs.jottacloud.com/jfs/{{username}}/Jotta/Sync` |  |
| [Get Userinfo](actions/get-userinfo.md) | `GET https://id.jottacloud.com/auth/realms/jottacloud/protocol/openid-connect/userinfo` | [docs](https://id.jottacloud.com/auth/realms/jottacloud/.well-known/openid-configuration) |
| [List Folder](actions/list-folder.md) | `POST /files/v2/list_folder` |  |
| [List Revisions](actions/list-revisions.md) | `POST /files/v2/list_revisions` |  |
| [Move Path](actions/move-path.md) | `POST /files/v2/move` |  |
| [Permanently Delete Path](actions/permanently-delete-path.md) | `POST /files/v2/permanently_delete` |  |
| [Ping Files API](actions/ping-files-api.md) | `POST /files/v2/ping` |  |
| [Restore Path](actions/restore-path.md) | `POST /files/v2/restore` |  |
