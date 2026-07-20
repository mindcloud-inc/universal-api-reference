# <img src="https://images.mindcloud.co/apps/icons/control-d_1776175011097.png" alt="Control D logo" width="28" height="28"> Control D: Universal API

Manage DNS profiles, endpoints, filters, and analytics

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/controlD/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://controld.com
- **Vendor API docs:** https://docs.controld.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Profiles](actions/list-profiles.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/controlD/latest/actions/list-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Custom Rule

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Rule](actions/create-custom-rule.md) | POST | Creates a custom rule in Control D. |
| [List Custom Rules](actions/list-custom-rules.md) | GET | Retrieves custom rules for a profile from Control D. |
| [Modify Custom Rule](actions/modify-custom-rule.md) | PUT | Updates a custom rule in Control D. |

### Default Rule

| Action | Method | Description |
| --- | --- | --- |
| [Get Default Rule](actions/get-default-rule.md) | GET | Retrieves the default rule from Control D. |
| [Modify Default Rule](actions/modify-default-rule.md) | PUT | Updates the default rule in Control D. |

### Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Create Endpoint](actions/create-endpoint.md) | POST | Creates an endpoint in Control D. |
| [List Endpoints](actions/list-endpoints.md) | GET | Retrieves endpoints from Control D. |
| [Modify Endpoint](actions/modify-endpoint.md) | PUT | Updates an endpoint in Control D. |

### Endpoint Type

| Action | Method | Description |
| --- | --- | --- |
| [List Endpoint Types](actions/list-endpoint-types.md) | GET | Retrieves endpoint types from Control D. |

### External Filter

| Action | Method | Description |
| --- | --- | --- |
| [List External Filters](actions/list-external-filters.md) | GET | Retrieves external filters for a profile from Control D. |

### Filter

| Action | Method | Description |
| --- | --- | --- |
| [Batch Modify Filters](actions/batch-modify-filters.md) | PUT | Updates multiple filters for a profile in Control D. |
| [List Native Filters](actions/list-native-filters.md) | GET | Retrieves native filters for a profile from Control D. |
| [Modify Filter](actions/modify-filter.md) | PUT | Updates a filter for a profile in Control D. |

### Ip Address

| Action | Method | Description |
| --- | --- | --- |
| [Get Current IP](actions/get-current-ip.md) | GET | Retrieves the current IP from Control D. |

### Known Ip

| Action | Method | Description |
| --- | --- | --- |
| [Learn New IP](actions/learn-new-ip.md) | POST | Creates a known IP in Control D. |
| [List Known IPs](actions/list-known-ips.md) | GET | Retrieves known IPs from Control D. |

### Log Level

| Action | Method | Description |
| --- | --- | --- |
| [List Log Levels](actions/list-log-levels.md) | GET | Retrieves log levels from Control D. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [List Organization Members](actions/list-organization-members.md) | GET | Retrieves organization members from Control D. |

### Network Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Network Stats](actions/get-network-stats.md) | GET | Retrieves network statistics from Control D. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Info](actions/get-organization-info.md) | GET | Retrieves organization details from Control D. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [List Payments](actions/list-payments.md) | GET | Retrieves payments from Control D. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [List Active Products](actions/list-active-products.md) | GET | Retrieves active products from Control D. |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Create Profile](actions/create-profile.md) | POST | Creates a profile in Control D. |
| [List Profiles](actions/list-profiles.md) | GET | Retrieves profiles from Control D. |
| [Modify Profile](actions/modify-profile.md) | PUT | Updates a profile in Control D. |

### Profile Option

| Action | Method | Description |
| --- | --- | --- |
| [List Profile Options](actions/list-profile-options.md) | GET | Retrieves profile options from Control D. |
| [Modify Profile Option](actions/modify-profile-option.md) | PUT | Updates a profile option in Control D. |

### Proxy

| Action | Method | Description |
| --- | --- | --- |
| [List Proxies](actions/list-proxies.md) | GET | Retrieves proxies from Control D. |

### Rule Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Rule Folder](actions/create-rule-folder.md) | POST | Creates a rule folder in Control D. |
| [List Rule Folders](actions/list-rule-folders.md) | GET | Retrieves rule folders for a profile from Control D. |
| [Modify Rule Folder](actions/modify-rule-folder.md) | PUT | Updates a rule folder in Control D. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [List Services In Category](actions/list-services-in-category.md) | GET | Retrieves services in a category from Control D. |

### Service Category

| Action | Method | Description |
| --- | --- | --- |
| [List Service Categories](actions/list-service-categories.md) | GET | Retrieves service categories from Control D. |

### Service Rule

| Action | Method | Description |
| --- | --- | --- |
| [List Profile Services](actions/list-profile-services.md) | GET | Retrieves services for a profile from Control D. |
| [Modify Profile Service](actions/modify-profile-service.md) | PUT | Updates a profile service in Control D. |

### Storage Region

| Action | Method | Description |
| --- | --- | --- |
| [List Storage Regions](actions/list-storage-regions.md) | GET | Retrieves storage regions from Control D. |

### Sub-organization

| Action | Method | Description |
| --- | --- | --- |
| [Create Sub-Organization](actions/create-sub-organization.md) | POST | Creates a sub-organization in Control D. |
| [List Sub-Organizations](actions/list-sub-organizations.md) | GET |  |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscriptions from Control D. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Data](actions/get-user-data.md) | GET | Retrieves user data from Control D. |

