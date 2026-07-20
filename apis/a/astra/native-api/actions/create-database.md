# Create Database with Astra

Creates a new database in Astra.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/databases`
- **Base URL:** `https://api.astra.datastax.com`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `capacityUnits` | body | `number` | no | Capacity units for the database. The verified workflow in this buildout uses 1. |
| `cloudProvider` | body | `string` | yes | The cloud provider, such as AWS, GCP, or AZURE. |
| `dbType` | body | `string` | no | The database type. The verified workflow in this buildout uses vector. |
| `keyspace` | body | `string` | no | Optional keyspace name. Leave empty to use Astra's default keyspace for vector databases. |
| `name` | body | `string` | yes | The database name. |
| `region` | body | `string` | yes | The deployment region. |
| `tier` | body | `string` | no | The Astra tier. The verified workflow in this buildout uses serverless. |
