# <img src="https://images.mindcloud.co/apps/icons/jottacloud_1774987274472.png" alt="Jottacloud logo" width="28" height="28"> Jottacloud: Universal API

Jottacloud is a cloud storage and backup service. This Stage 1 draft is currently anchored to Jottacloud's verified identity/session surface and uses the official OpenID Connect userinfo endpoint for initial auth validation.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/jottacloud/latest
- **Category:** Content & Files / Storage
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.jottacloud.com/
- **Vendor API docs:** https://docs.jottacloud.com/en/collections/178055-our-command-line-tool

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Userinfo](actions/get-userinfo.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jottacloud/latest/actions/get-userinfo?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Root](actions/get-account-root.md) | GET |  |
| [Get Archive Mount](actions/get-archive-mount.md) | GET |  |
| [Get Jotta Device Root](actions/get-jotta-device-root.md) | GET |  |
| [Get Sync Mount](actions/get-sync-mount.md) | GET |  |

### Public Share

| Action | Method | Description |
| --- | --- | --- |
| [Disable Public Share](actions/disable-public-share.md) | DELETE |  |
| [Enable Public Share](actions/enable-public-share.md) | POST |  |
| [Get Share Info](actions/get-share-info.md) | GET |  |

### Storage Path

| Action | Method | Description |
| --- | --- | --- |
| [Copy Path](actions/copy-path.md) | POST |  |
| [Create Folder](actions/create-folder.md) | POST |  |
| [Delete Path](actions/delete-path.md) | DELETE |  |
| [Get Path](actions/get-path.md) | GET |  |
| [List Folder](actions/list-folder.md) | GET |  |
| [List Revisions](actions/list-revisions.md) | GET |  |
| [Move Path](actions/move-path.md) | PUT |  |
| [Permanently Delete Path](actions/permanently-delete-path.md) | DELETE |  |
| [Ping Files API](actions/ping-files-api.md) | GET |  |
| [Restore Path](actions/restore-path.md) | PUT |  |

### User Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Userinfo](actions/get-userinfo.md) | GET |  |

