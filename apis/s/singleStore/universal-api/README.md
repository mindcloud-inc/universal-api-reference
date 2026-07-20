# <img src="https://images.mindcloud.co/apps/icons/single-store_1775574975447.png" alt="SingleStore logo" width="28" height="28"> SingleStore: Universal API

SingleStore Flow on Helios Ingest wrapper for configuring source and destination database connections, schedules, table selection, and ingest operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/singleStore/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.singlestore.com/
- **Vendor API docs:** https://docs.singlestore.com/cloud/load-data/load-data-with-singlestore-flow-on-helios/flow-on-helios-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Schedule Settings](actions/get-schedule-settings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/singleStore/latest/actions/get-schedule-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Get Destination Database Details](actions/get-destination-database-details.md) | GET | Retrieves destination database details from SingleStore. |
| [Get Source Database Details](actions/get-source-database-details.md) | GET | Retrieves source database details from SingleStore. |
| [Save Destination Database Configuration](actions/save-destination-database-configuration.md) | PUT | Updates the destination database configuration in SingleStore. |
| [Save Source Database Configuration](actions/save-source-database-configuration.md) | PUT | Updates the source database configuration in SingleStore. |
| [Test Destination Database Connection](actions/test-destination-database-connection.md) | GET | Tests the destination database connection in SingleStore. |
| [Test Source Database Connection](actions/test-source-database-connection.md) | GET | Tests the source database connection in SingleStore. |

### Data Syncs

| Action | Method | Description |
| --- | --- | --- |
| [Execute an Operation in Ingest](actions/execute-an-operation-in-ingest.md) | POST | Executes an ingest operation in SingleStore. |

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [List Available Tables with Selection Status](actions/list-available-tables-with-selection-status.md) | GET | Retrieves available source tables and their ingestion selection status from SingleStore. |
| [Select a Table for Ingestion](actions/select-a-table-for-ingestion.md) | PUT | Updates whether a source table is selected for ingestion in SingleStore. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Get Schedule Settings](actions/get-schedule-settings.md) | GET | Retrieves schedule settings from SingleStore. |
| [Save Schedule Settings](actions/save-schedule-settings.md) | PUT | Updates schedule settings in SingleStore. |

