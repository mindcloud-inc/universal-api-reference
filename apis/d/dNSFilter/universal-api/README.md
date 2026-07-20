# <img src="https://images.mindcloud.co/apps/icons/d-nsfilter_1774023225394.png" alt="DNSFilter logo" width="28" height="28"> DNSFilter: Universal API

Protect networks, block threats, and manage DNS filtering policies

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dNSFilter/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.dnsfilter.com/
- **Vendor API docs:** https://api.dnsfilter.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Networks](actions/list-networks.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/list-networks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Get Application](actions/get-application.md) | GET |  |
| [List All Applications](actions/list-all-applications.md) | GET |  |
| [List Applications](actions/list-applications.md) | GET |  |

### Application Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Application Category](actions/get-application-category.md) | GET |  |
| [List Application Categories](actions/list-application-categories.md) | GET |  |

### Block Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Block Page](actions/get-block-page.md) | GET |  |
| [List Block Pages](actions/list-block-pages.md) | GET |  |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Category](actions/get-category.md) | GET |  |
| [List All Categories](actions/list-all-categories.md) | GET |  |
| [List Categories](actions/list-categories.md) | GET |  |

### Domain Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Lookup Domains](actions/bulk-lookup-domains.md) | GET |  |
| [Lookup Domain](actions/lookup-domain.md) | GET |  |

### Domain Note

| Action | Method | Description |
| --- | --- | --- |
| [Get Domain Note](actions/get-domain-note.md) | GET |  |

### Ip Address

| Action | Method | Description |
| --- | --- | --- |
| [Get IP Address](actions/get-ip-address.md) | GET |  |
| [List All IP Addresses](actions/list-all-ip-addresses.md) | GET |  |
| [List IP Addresses](actions/list-ip-addresses.md) | GET |  |

### Ip Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify IP Address](actions/verify-ip-address.md) | GET |  |

### Mac Address

| Action | Method | Description |
| --- | --- | --- |
| [Get MAC Address](actions/get-mac-address.md) | GET |  |
| [List All MAC Addresses](actions/list-all-mac-addresses.md) | GET |  |
| [List MAC Addresses](actions/list-mac-addresses.md) | GET |  |

### Network

| Action | Method | Description |
| --- | --- | --- |
| [Get Network](actions/get-network.md) | GET |  |
| [List All Networks](actions/list-all-networks.md) | GET |  |
| [List Networks](actions/list-networks.md) | GET |  |

### Network Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Network Counts](actions/get-network-counts.md) | GET |  |

### Network Geo

| Action | Method | Description |
| --- | --- | --- |
| [Get Network Geo](actions/get-network-geo.md) | GET |  |

### Network Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Network](actions/lookup-network.md) | GET |  |

### Network Subnet

| Action | Method | Description |
| --- | --- | --- |
| [Get Network Subnet](actions/get-network-subnet.md) | GET |  |
| [List Network Subnets](actions/list-network-subnets.md) | GET |  |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET |  |
| [List All Organizations](actions/list-all-organizations.md) | GET |  |
| [List Organizations](actions/list-organizations.md) | GET |  |

### Organization Setting

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Settings](actions/get-organization-settings.md) | GET |  |

### Organization User

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization User](actions/get-organization-user.md) | GET |  |
| [List Organization Users](actions/list-organization-users.md) | GET |  |

### Policy

| Action | Method | Description |
| --- | --- | --- |
| [Get Policy](actions/get-policy.md) | GET |  |
| [List All Policies](actions/list-all-policies.md) | GET |  |
| [List Policies](actions/list-policies.md) | GET |  |

### Policy Application

| Action | Method | Description |
| --- | --- | --- |
| [Get Policy Application](actions/get-policy-application.md) | GET |  |

### Policy Permissive Mode

| Action | Method | Description |
| --- | --- | --- |
| [Get Policy Permissive Mode](actions/get-policy-permissive-mode.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |

