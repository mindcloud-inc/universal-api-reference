# SingleStore: Native API Reference

A consolidated summary of SingleStore's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://docs.singlestore.com/cloud/load-data/load-data-with-singlestore-flow-on-helios/flow-on-helios-api/
- **API base URL:** `https://{flowEndpoint}:30081/ingest/api/ingest`

## Authentication

### API Key

Use a SingleStore Flow on Helios API key in the default Bearer Authorization header.

### Credentials

- **API Key:** `apiKey` · required
- **Flow Endpoint:** `flowEndpoint` · required · SingleStore Flow host name without protocol or port, for example svc-...-flow.aws-<region>.svc.singlestore.com.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.singlestore.com/cloud/load-data/load-data-with-singlestore-flow-on-helios/flow-on-helios-api/flow-on-helios-api-authentication/)

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Execute an Operation in Ingest](actions/execute-an-operation-in-ingest.md) | `POST /ops/extract/{operation}` | [docs](https://docs.singlestore.com/cloud/load-data/load-data-with-singlestore-flow-on-helios/flow-on-helios-api/flow-on-helios-ingest-api/#execute-an-operation-in-ingest) |
| [Get Destination Database Details](actions/get-destination-database-details.md) | `GET /conn-dst` | [docs](https://docs.singlestore.com/cloud/load-data/load-data-with-singlestore-flow-on-helios/flow-on-helios-api/flow-on-helios-ingest-api/#get-destination-database-details) |
| [Get Schedule Settings](actions/get-schedule-settings.md) | `GET /config-sched` | [docs](https://docs.singlestore.com/cloud/load-data/load-data-with-singlestore-flow-on-helios/flow-on-helios-api/flow-on-helios-ingest-api/#get-schedule-settings) |
| [Get Source Database Details](actions/get-source-database-details.md) | `GET /conn-src` | [docs](https://docs.singlestore.com/cloud/load-data/load-data-with-singlestore-flow-on-helios/flow-on-helios-api/flow-on-helios-ingest-api/#get-source-database-details) |
| [List Available Tables with Selection Status](actions/list-available-tables-with-selection-status.md) | `GET /list-db/{database}/{schema}` | [docs](https://docs.singlestore.com/cloud/load-data/load-data-with-singlestore-flow-on-helios/flow-on-helios-api/flow-on-helios-ingest-api/#list-available-tables-with-selection-status) |
| [Save Destination Database Configuration](actions/save-destination-database-configuration.md) | `PATCH /conn-dst` | [docs](https://docs.singlestore.com/cloud/load-data/load-data-with-singlestore-flow-on-helios/flow-on-helios-api/flow-on-helios-ingest-api/#save-destination-database-configuration) |
| [Save Schedule Settings](actions/save-schedule-settings.md) | `PATCH /config-sched` | [docs](https://docs.singlestore.com/cloud/load-data/load-data-with-singlestore-flow-on-helios/flow-on-helios-api/flow-on-helios-ingest-api/#save-schedule-settings) |
| [Save Source Database Configuration](actions/save-source-database-configuration.md) | `PATCH /conn-src` | [docs](https://docs.singlestore.com/cloud/load-data/load-data-with-singlestore-flow-on-helios/flow-on-helios-api/flow-on-helios-ingest-api/#save-source-database-configuration) |
| [Select a Table for Ingestion](actions/select-a-table-for-ingestion.md) | `PATCH /config-tab/{database}/{schema}/{table}` | [docs](https://docs.singlestore.com/cloud/load-data/load-data-with-singlestore-flow-on-helios/flow-on-helios-api/flow-on-helios-ingest-api/#select-a-table-for-ingestion) |
| [Test Destination Database Connection](actions/test-destination-database-connection.md) | `POST /conn-dst/test` | [docs](https://docs.singlestore.com/cloud/load-data/load-data-with-singlestore-flow-on-helios/flow-on-helios-api/flow-on-helios-ingest-api/#test-destination-database-connection) |
| [Test Source Database Connection](actions/test-source-database-connection.md) | `POST /conn-src/test` | [docs](https://docs.singlestore.com/cloud/load-data/load-data-with-singlestore-flow-on-helios/flow-on-helios-api/flow-on-helios-ingest-api/#test-source-database-connection) |
