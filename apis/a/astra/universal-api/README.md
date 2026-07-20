# <img src="https://images.mindcloud.co/apps/icons/ibm-logo_1780949399106.png" alt="Astra logo" width="28" height="28"> Astra: Universal API

Manage Astra organizations, databases, roles, and tokens

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/astra/latest
- **Category:** IT Operations / Database
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ibm.com/products/datastax
- **Vendor API docs:** https://docs.datastax.com/en/astra-api-docs/_attachments/devops-api/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Org](actions/get-current-org.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/astra/latest/actions/get-current-org?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Database

| Action | Method | Description |
| --- | --- | --- |
| [Create Database](actions/create-database.md) | POST | Creates a new database in Astra. |
| [Get Database](actions/get-database.md) | GET | Retrieves one Astra database by ID. |
| [List Databases](actions/list-databases.md) | GET | Retrieves database records from Astra. |

### Database Datacenter

| Action | Method | Description |
| --- | --- | --- |
| [List Database Datacenters](actions/list-database-datacenters.md) | GET | Retrieves datacenters for an Astra database. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Org](actions/get-current-org.md) | GET | Retrieves the current organization from Astra. |

### Organization User

| Action | Method | Description |
| --- | --- | --- |
| [List Organization Users](actions/list-organization-users.md) | GET | Retrieves organization users from Astra. |

### Private Link

| Action | Method | Description |
| --- | --- | --- |
| [Get Datacenter Private Link](actions/get-datacenter-private-link.md) | GET | Retrieves private link details for an Astra datacenter. |
| [List Organization Private Links](actions/list-organization-private-links.md) | GET | Retrieves private link connections for an Astra organization. |

### Region

| Action | Method | Description |
| --- | --- | --- |
| [List Available Regions](actions/list-available-regions.md) | GET | Retrieves available Astra serverless regions. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization User](actions/get-organization-user.md) | GET | Retrieves one organization user from Astra. |

