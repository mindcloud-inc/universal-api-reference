# <img src="https://images.mindcloud.co/apps/icons/qye5c-cf_1781723678011.png" alt="Docusnap365 logo" width="28" height="28"> Docusnap365: Universal API

Access Docusnap365's IT inventory, infrastructure, and asset data through its REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/docusnap365/latest
- **Category:** IT Operations / IT Service Management
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.docusnap.com/en
- **Vendor API docs:** https://api-doc.docusnap.com/reference/first-steps

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sites](actions/list-sites.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docusnap365/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Details](actions/get-data-details.md) | GET |  |
| [List Data](actions/list-data.md) | GET |  |
| [List Data By Type](actions/list-data-by-type.md) | GET |  |

### Data Type

| Action | Method | Description |
| --- | --- | --- |
| [List Data Types](actions/list-data-types.md) | GET |  |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [List Domains](actions/list-domains.md) | GET |  |

### Network

| Action | Method | Description |
| --- | --- | --- |
| [Get Network Details](actions/get-network-details.md) | GET |  |
| [List Networks](actions/list-networks.md) | GET |  |
| [List Networks By Type](actions/list-networks-by-type.md) | GET |  |

### Network Type

| Action | Method | Description |
| --- | --- | --- |
| [List Network Types](actions/list-network-types.md) | GET |  |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET |  |

### Platform

| Action | Method | Description |
| --- | --- | --- |
| [List Platforms](actions/list-platforms.md) | GET |  |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [Get Service Details](actions/get-service-details.md) | GET |  |
| [List Services](actions/list-services.md) | GET |  |
| [List Services By Type](actions/list-services-by-type.md) | GET |  |

### Service Type

| Action | Method | Description |
| --- | --- | --- |
| [List Service Types](actions/list-service-types.md) | GET |  |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [List Sites](actions/list-sites.md) | GET |  |

### System

| Action | Method | Description |
| --- | --- | --- |
| [Get System Details](actions/get-system-details.md) | GET |  |
| [List Systems](actions/list-systems.md) | GET |  |
| [List Systems By Type](actions/list-systems-by-type.md) | GET |  |

### System Type

| Action | Method | Description |
| --- | --- | --- |
| [List System Types](actions/list-system-types.md) | GET |  |

