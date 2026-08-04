# <img src="https://images.mindcloud.co/apps/icons/toastlogo-web-color_1769700023917.jpeg" alt="Toast logo" width="28" height="28"> Toast: Universal API

Connect to Toast to retrieve restaurant, menu, order, labor, and configuration data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/toast/latest
- **Category:** Commerce
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pos.toasttab.com
- **Vendor API docs:** https://doc.toasttab.com/openapi/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Dining Option](actions/get-dining-option.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toast/latest/actions/get-dining-option?connectionId=$CONNECTION_ID&guid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Dining Option

| Action | Method | Description |
| --- | --- | --- |
| [Get Dining Option](actions/get-dining-option.md) | GET | Retrieves one dining option by Toast GUID. |
| [List Dining Options](actions/list-dining-options.md) | GET | Retrieves dining options configured for the connected restaurant. |

### Discounts

| Action | Method | Description |
| --- | --- | --- |
| [Get Discount](actions/get-discount.md) | GET | Retrieves one discount by Toast GUID. |
| [List Discounts](actions/list-discounts.md) | GET | Retrieves discounts configured for the connected restaurant. |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Get Employee](actions/get-employee.md) | GET | Retrieves one employee by Toast GUID or external identifier. |
| [List Employees](actions/list-employees.md) | GET | Retrieves employees for the connected restaurant, optionally limited to specific identifiers. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Get Job](actions/get-job.md) | GET | Retrieves one labor job by Toast GUID or external identifier. |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves labor jobs for the connected restaurant, optionally limited to specific identifiers. |

### Menu

| Action | Method | Description |
| --- | --- | --- |
| [Get Menus](actions/get-menus.md) | GET | Retrieves the fully resolved set of published menus for the connected restaurant. |

### Menu Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Menu Item](actions/get-menu-item.md) | GET | Retrieves one menu item or modifier by Toast GUID. |
| [List Menu Items](actions/list-menu-items.md) | GET | Retrieves menu items and modifiers configured for the connected restaurant. |

### Menu Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Menu Metadata](actions/get-menu-metadata.md) | GET | Retrieves the last-modified timestamp for published menu data. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET | Retrieves one order by its Toast GUID. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders for the connected restaurant using a date selector and paginated results. |

### Restaurant

| Action | Method | Description |
| --- | --- | --- |
| [Get Restaurant](actions/get-restaurant.md) | GET |  |

### Revenue Center

| Action | Method | Description |
| --- | --- | --- |
| [List Revenue Centers](actions/list-revenue-centers.md) | GET | Retrieves revenue centers configured for the connected restaurant. |

### Sales Category

| Action | Method | Description |
| --- | --- | --- |
| [List Sales Categories](actions/list-sales-categories.md) | GET | Retrieves menu-item sales categories configured for the connected restaurant. |

### Service Area

| Action | Method | Description |
| --- | --- | --- |
| [List Service Areas](actions/list-service-areas.md) | GET | Retrieves service areas configured for the connected restaurant. |

### Service Charge

| Action | Method | Description |
| --- | --- | --- |
| [List Service Charges](actions/list-service-charges.md) | GET | Retrieves service charges configured for the connected restaurant. |

### Shift

| Action | Method | Description |
| --- | --- | --- |
| [Get Shift](actions/get-shift.md) | GET | Retrieves one labor shift by Toast GUID or external identifier. |
| [List Shifts](actions/list-shifts.md) | GET | Retrieves labor shifts by identifier or by an ISO-8601 date range of up to one month. |

### Tax Rates

| Action | Method | Description |
| --- | --- | --- |
| [List Tax Rates](actions/list-tax-rates.md) | GET | Retrieves tax rates configured for the connected restaurant. |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [Get Time Entry](actions/get-time-entry.md) | GET | Retrieves one employee time entry by Toast GUID or external identifier. |
| [List Time Entries](actions/list-time-entries.md) | GET | Retrieves employee time entries using identifiers, date ranges, modification ranges, or business date. |

