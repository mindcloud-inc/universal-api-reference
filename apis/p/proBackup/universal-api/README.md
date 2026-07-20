# <img src="https://images.mindcloud.co/apps/icons/pro-backup_1775851502868.png" alt="ProBackup logo" width="28" height="28"> ProBackup: Universal API

ProBackup is a SaaS backup and restore platform for cloud apps. Verified external API evidence currently shows a narrow Make.com API-key surface plus a richer authenticated product API used by the web app.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/proBackup/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.probackup.io
- **Vendor API docs:** https://apps.make.com/pro-backup

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Platforms](actions/list-platforms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proBackup/latest/actions/list-platforms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Platform

| Action | Method | Description |
| --- | --- | --- |
| [List Platforms](actions/list-platforms.md) | GET | Retrieves active backup platforms from ProBackup. |

