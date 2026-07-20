# List transactions with Appwrite

Retrieves a list of transactions from your Appwrite project.

## Endpoint

- **Method:** `GET`
- **Path:** `/tablesdb/transactions`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [List transactions](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queries[]` | query | `array<string>` | no | Array of query strings generated using the Query class provided by the SDK. [Learn more about queries](https://appwrite.io/docs/queries). Send multiple values as a array. |
