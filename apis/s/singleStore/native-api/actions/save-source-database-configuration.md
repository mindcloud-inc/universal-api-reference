# Save Source Database Configuration with SingleStore

Updates the source database configuration in SingleStore.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/conn-src`
- **Base URL:** `https://{flowEndpoint}:30081/ingest/api/ingest`
- **Official documentation:** [Save Source Database Configuration](https://docs.singlestore.com/cloud/load-data/load-data-with-singlestore-flow-on-helios/flow-on-helios-api/flow-on-helios-ingest-api/#save-source-database-configuration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `host` | body | `string` | yes | Hostname or IP address of the source database server. |
| `port` | body | `number` | yes | Port number for the source database server. |
| `uid` | body | `string` | yes | Database username for the source connection. |
| `type` | body | `string` | yes | SingleStore database type identifier for the source connection, for example mysql. |
