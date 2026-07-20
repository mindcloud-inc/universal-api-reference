# Test Source Database Connection with SingleStore

Tests the source database connection in SingleStore.

## Endpoint

- **Method:** `POST`
- **Path:** `/conn-src/test`
- **Base URL:** `https://{flowEndpoint}:30081/ingest/api/ingest`
- **Official documentation:** [Test Source Database Connection](https://docs.singlestore.com/cloud/load-data/load-data-with-singlestore-flow-on-helios/flow-on-helios-api/flow-on-helios-ingest-api/#test-source-database-connection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `host` | body | `string` | yes | Hostname or IP address of the source database server. |
| `port` | body | `number` | yes | Port number for the source database server. |
| `uid` | body | `string` | yes | Database username for the source connection. |
| `type` | body | `string` | yes | SingleStore database type identifier for the source connection, for example mysql. |
