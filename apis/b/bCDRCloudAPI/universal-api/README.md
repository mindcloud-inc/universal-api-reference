# <img src="https://images.mindcloud.co/apps/icons/b-icon_1776095579366.png" alt="BCDR Cloud logo" width="28" height="28"> BCDR Cloud: Universal API

Cloud-based BDRShield management console for backup, recovery, reporting, and infrastructure operations across endpoints, servers, VMs, SaaS, and databases.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bCDRCloudAPI/latest
- **Category:** IT Operations / IT Service Management
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.bdrshield.com/
- **Vendor API docs:** https://support.bdrshield.com/portal/en/kb/articles/api-management-execution

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Portal Server](actions/get-portal-server.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bCDRCloudAPI/latest/actions/get-portal-server?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Config Values

| Action | Method | Description |
| --- | --- | --- |
| [Get Config Values](actions/get-config-values.md) | GET |  |

### Notifications Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Notifications Count](actions/get-notifications-count.md) | GET |  |

### Portal Server

| Action | Method | Description |
| --- | --- | --- |
| [Get Portal Server](actions/get-portal-server.md) | GET |  |

### Product Labels

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Labels](actions/get-product-labels.md) | GET |  |

