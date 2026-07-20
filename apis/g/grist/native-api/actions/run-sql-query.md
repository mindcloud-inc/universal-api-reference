# Run SQL Query with Grist

Runs a SQL query in a Grist document.

## Endpoint

- **Method:** `POST`
- **Path:** `/docs/:docId/sql`
- **Base URL:** `https://docs.getgrist.com/api`
- **Official documentation:** [Run SQL Query](https://support.getgrist.com/api/#tag/sql/operation/runSql)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document ID |
| `sql` | body | `string` | yes | SQL query to execute |
| `timeout` | body | `number` | no | Query timeout in ms |
