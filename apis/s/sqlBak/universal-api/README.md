# <img src="https://images.mindcloud.co/apps/icons/sql-bak_1777305218562.png" alt="SqlBak logo" width="28" height="28"> SqlBak: Universal API

Manage database backups, servers, jobs, and backup health

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sqlBak/latest
- **Category:** IT Operations / Database
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sqlbak.com/
- **Vendor API docs:** https://sqlbak.docs.apiary.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Information](actions/get-account-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sqlBak/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Information](actions/get-account-information.md) | GET | Retrieves account information from SqlBak. |

### Dbms Connection

| Action | Method | Description |
| --- | --- | --- |
| [List DBMS Connections](actions/list-dbms-connections.md) | GET | Retrieves DBMS connections from SqlBak. |

### Destination

| Action | Method | Description |
| --- | --- | --- |
| [List Destinations](actions/list-destinations.md) | GET | Retrieves destinations from SqlBak. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves jobs from SqlBak. |

### Server

| Action | Method | Description |
| --- | --- | --- |
| [List Servers](actions/list-servers.md) | GET | Retrieves servers from SqlBak. |

