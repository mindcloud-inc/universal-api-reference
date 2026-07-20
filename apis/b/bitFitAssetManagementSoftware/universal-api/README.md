# <img src="https://images.mindcloud.co/apps/icons/bitfit-icon_1775660439542.png" alt="bitFit Asset Management Software logo" width="28" height="28"> bitFit Asset Management Software: Universal API

BitFit Asset Management Software integrates with the BitFit asset management API for assets, locations, users, service requests, attachments, widgets, and related inventory data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bitFitAssetManagementSoftware/latest
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://assets.bitfit.com/
- **Vendor API docs:** https://assets.bitfit.com/setup/api/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Assets](actions/list-assets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitFitAssetManagementSoftware/latest/actions/list-assets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Asset

| Action | Method | Description |
| --- | --- | --- |
| [List Assets](actions/list-assets.md) | GET |  |

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Get Asset](actions/get-asset.md) | GET |  |

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Get Attachment](actions/get-attachment.md) | GET |  |
| [List Attachments](actions/list-attachments.md) | GET |  |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET |  |
| [List Companies](actions/list-companies.md) | GET |  |

### Dashboards

| Action | Method | Description |
| --- | --- | --- |
| [Get Widget](actions/get-widget.md) | GET |  |
| [List Widgets](actions/list-widgets.md) | GET |  |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Get Group](actions/get-group.md) | GET |  |
| [List Groups](actions/list-groups.md) | GET |  |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Get Consumable](actions/get-consumable.md) | GET |  |
| [List Consumables](actions/list-consumables.md) | GET |  |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Get List](actions/get-list.md) | GET |  |
| [List Lists](actions/list-lists.md) | GET |  |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Get Location](actions/get-location.md) | GET |  |
| [List Locations](actions/list-locations.md) | GET |  |

### Models

| Action | Method | Description |
| --- | --- | --- |
| [Get Config](actions/get-config.md) | GET |  |
| [List Configs](actions/list-configs.md) | GET |  |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Get Page](actions/get-page.md) | GET |  |
| [List Pages](actions/list-pages.md) | GET |  |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [Get Role](actions/get-role.md) | GET |  |
| [List Roles](actions/list-roles.md) | GET |  |

### Service Requests

| Action | Method | Description |
| --- | --- | --- |
| [Get Request](actions/get-request.md) | GET |  |
| [List Requests](actions/list-requests.md) | GET |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Inventory Rule](actions/get-inventory-rule.md) | GET |  |
| [Get Widget Config](actions/get-widget-config.md) | GET |  |
| [List Inventory Rules](actions/list-inventory-rules.md) | GET |  |
| [List Widget Configs](actions/list-widget-configs.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |

