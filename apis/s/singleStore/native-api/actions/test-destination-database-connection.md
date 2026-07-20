# Test Destination Database Connection with SingleStore

Tests the destination database connection in SingleStore.

## Endpoint

- **Method:** `POST`
- **Path:** `/conn-dst/test`
- **Base URL:** `https://{flowEndpoint}:30081/ingest/api/ingest`
- **Official documentation:** [Test Destination Database Connection](https://docs.singlestore.com/cloud/load-data/load-data-with-singlestore-flow-on-helios/flow-on-helios-api/flow-on-helios-ingest-api/#test-destination-database-connection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `host` | body | `string` | yes | Hostname or IP address of the destination database server. |
| `port` | body | `number` | yes | Port number for the destination database server. |
| `uid` | body | `string` | yes | Database username for the destination connection. |
| `type` | body | `string` | yes | SingleStore database type identifier for the destination connection, for example mysql. |
