# Save Destination Database Configuration with SingleStore

Updates the destination database configuration in SingleStore.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/conn-dst`
- **Base URL:** `https://{flowEndpoint}:30081/ingest/api/ingest`
- **Official documentation:** [Save Destination Database Configuration](https://docs.singlestore.com/cloud/load-data/load-data-with-singlestore-flow-on-helios/flow-on-helios-api/flow-on-helios-ingest-api/#save-destination-database-configuration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `host` | body | `string` | yes | Hostname or IP address of the destination database server. |
| `port` | body | `number` | yes | Port number for the destination database server. |
| `uid` | body | `string` | yes | Database username for the destination connection. |
| `type` | body | `string` | yes | SingleStore database type identifier for the destination connection, for example mysql. |
