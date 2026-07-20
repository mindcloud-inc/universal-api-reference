# <img src="https://images.mindcloud.co/apps/icons/images-35_1774977499250.png" alt="IronWiFi logo" width="28" height="28"> IronWiFi: Universal API

Manage IronWiFi users, vouchers, captive portals, access infrastructure, and reporting through the IronWiFi REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ironWiFi/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ironwifi.com/
- **Vendor API docs:** https://api.ironwifi.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ironWiFi/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Access_point

| Action | Method | Description |
| --- | --- | --- |
| [List Access Points](actions/list-access-points.md) | GET | Retrieves access points from IronWiFi. |

### Accounting_report

| Action | Method | Description |
| --- | --- | --- |
| [Get Accounting Report](actions/get-accounting-report.md) | GET | Retrieves RADIUS accounting logs from IronWiFi. |

### Attribute

| Action | Method | Description |
| --- | --- | --- |
| [List Attributes](actions/list-attributes.md) | GET | Retrieves attributes for a specific table from IronWiFi. |

### Authentication_report

| Action | Method | Description |
| --- | --- | --- |
| [Get Authentication Report](actions/get-authentication-report.md) | GET | Retrieves RADIUS authentication logs from IronWiFi. |

### Captive_portal

| Action | Method | Description |
| --- | --- | --- |
| [List Captive Portals](actions/list-captive-portals.md) | GET | Retrieves captive portals from IronWiFi. |

### Configuration

| Action | Method | Description |
| --- | --- | --- |
| [List Configurations](actions/list-configurations.md) | GET | Retrieves configurations from IronWiFi. |

### Connector

| Action | Method | Description |
| --- | --- | --- |
| [List Connectors](actions/list-connectors.md) | GET | Retrieves connectors from IronWiFi. |

### Device

| Action | Method | Description |
| --- | --- | --- |
| [List Devices](actions/list-devices.md) | GET | Retrieves devices from IronWiFi. |

### Employee

| Action | Method | Description |
| --- | --- | --- |
| [List Employees](actions/list-employees.md) | GET | Retrieves employees from IronWiFi. |

### Fleet

| Action | Method | Description |
| --- | --- | --- |
| [List Fleets](actions/list-fleets.md) | GET | Retrieves fleets from IronWiFi. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from IronWiFi. |

### Guest

| Action | Method | Description |
| --- | --- | --- |
| [List Guests](actions/list-guests.md) | GET | Retrieves guests from IronWiFi. |

### Guest_profile

| Action | Method | Description |
| --- | --- | --- |
| [List Guest Profiles](actions/list-guest-profiles.md) | GET | Retrieves guest profiles from IronWiFi. |

### Network

| Action | Method | Description |
| --- | --- | --- |
| [List Networks](actions/list-networks.md) | GET | Retrieves networks from IronWiFi. |

### Organization_unit

| Action | Method | Description |
| --- | --- | --- |
| [List Organization Units](actions/list-organization-units.md) | GET | Retrieves organization units from IronWiFi. |

### Organization_unit_group_mapping

| Action | Method | Description |
| --- | --- | --- |
| [List Org Unit Group Mappings](actions/list-org-unit-group-mappings.md) | GET | Retrieves organization unit group mappings from IronWiFi. |

### Shared_file

| Action | Method | Description |
| --- | --- | --- |
| [List Shared Files](actions/list-shared-files.md) | GET | Retrieves shared files from IronWiFi. |

### Tariff

| Action | Method | Description |
| --- | --- | --- |
| [List Tariffs](actions/list-tariffs.md) | GET | Retrieves tariffs from IronWiFi. |

### Tariff_group

| Action | Method | Description |
| --- | --- | --- |
| [List Tariff Groups](actions/list-tariff-groups.md) | GET | Retrieves tariff groups from IronWiFi. |

### Theme

| Action | Method | Description |
| --- | --- | --- |
| [List Themes](actions/list-themes.md) | GET | Retrieves themes from IronWiFi. |

### Translation

| Action | Method | Description |
| --- | --- | --- |
| [List Translations](actions/list-translations.md) | GET | Retrieves translations from IronWiFi. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from IronWiFi. |

### Variable

| Action | Method | Description |
| --- | --- | --- |
| [List Variables](actions/list-variables.md) | GET | Retrieves variables from IronWiFi. |

### Vehicle

| Action | Method | Description |
| --- | --- | --- |
| [List Vehicles](actions/list-vehicles.md) | GET | Retrieves vehicles from IronWiFi. |

### Venue

| Action | Method | Description |
| --- | --- | --- |
| [List Venues](actions/list-venues.md) | GET | Retrieves venues from IronWiFi. |

### Voucher

| Action | Method | Description |
| --- | --- | --- |
| [List Vouchers](actions/list-vouchers.md) | GET | Retrieves vouchers from IronWiFi. |

