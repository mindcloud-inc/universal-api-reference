# <img src="https://images.mindcloud.co/apps/icons/favicon-25_1777052345603.png" alt="Mews logo" width="28" height="28"> Mews: Universal API

Cloud hospitality platform for managing property operations, reservations, payments, and guest experiences with Mews Operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mews/latest
- **Category:** Commerce / ERP
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.mews.com/
- **Vendor API docs:** https://docs.mews.com/connector-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Configuration](actions/get-configuration.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Accounting Category

| Action | Method | Description |
| --- | --- | --- |
| [Get All Accounting Categories](actions/get-all-accounting-categories.md) | GET | Retrieves accounting categories from Mews. |

### Age Category

| Action | Method | Description |
| --- | --- | --- |
| [Get All Age Categories](actions/get-all-age-categories.md) | GET | Retrieves age categories from Mews. |

### Business Segment

| Action | Method | Description |
| --- | --- | --- |
| [Get All Business Segments](actions/get-all-business-segments.md) | GET | Retrieves business segments from Mews. |

### Cashier

| Action | Method | Description |
| --- | --- | --- |
| [Get All Cashiers](actions/get-all-cashiers.md) | GET | Retrieves cashiers from Mews. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get All Companies](actions/get-all-companies.md) | GET | Retrieves companies from Mews. |

### Counter

| Action | Method | Description |
| --- | --- | --- |
| [Get All Counters](actions/get-all-counters.md) | GET | Retrieves counters from Mews. |

### Currency

| Action | Method | Description |
| --- | --- | --- |
| [Get All Currencies](actions/get-all-currencies.md) | GET | Retrieves currencies from Mews. |

### Department

| Action | Method | Description |
| --- | --- | --- |
| [Get All Departments](actions/get-all-departments.md) | GET | Retrieves departments from Mews. |

### Enterprise Configuration

| Action | Method | Description |
| --- | --- | --- |
| [Get Configuration](actions/get-configuration.md) | GET | Retrieves enterprise configuration from Mews. |

### Exchange Rate

| Action | Method | Description |
| --- | --- | --- |
| [Get All Exchange Rates](actions/get-all-exchange-rates.md) | GET | Retrieves exchange rates from Mews. |

### Language

| Action | Method | Description |
| --- | --- | --- |
| [Get All Languages](actions/get-all-languages.md) | GET | Retrieves languages from Mews. |

### Outlet

| Action | Method | Description |
| --- | --- | --- |
| [Get All Outlets](actions/get-all-outlets.md) | GET | Retrieves outlets from Mews. |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [Get All Resources](actions/get-all-resources.md) | GET | Retrieves resources from Mews. |

### Resource Category

| Action | Method | Description |
| --- | --- | --- |
| [Get All Resource Categories](actions/get-all-resource-categories.md) | GET | Retrieves resource categories from Mews. |

### Resource Feature

| Action | Method | Description |
| --- | --- | --- |
| [Get All Resource Features](actions/get-all-resource-features.md) | GET | Retrieves resource features from Mews. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [Get All Services](actions/get-all-services.md) | GET | Retrieves services from Mews. |

### Source

| Action | Method | Description |
| --- | --- | --- |
| [Get All Sources](actions/get-all-sources.md) | GET | Retrieves reservation sources from Mews. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Add Task](actions/add-task.md) | POST | Creates a new task in Mews. |
| [Get All Tasks](actions/get-all-tasks.md) | GET | Retrieves tasks from Mews. |

### Tax Environment

| Action | Method | Description |
| --- | --- | --- |
| [Get All Tax Environments](actions/get-all-tax-environments.md) | GET | Retrieves tax environments from Mews. |

