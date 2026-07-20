# Merge Rows with Firebolt

Creates row merges in Firebolt.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineHost`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Merge Rows](https://docs.firebolt.io/reference-sql/commands/data-management/merge)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineHost` | path | `string` | yes | Firebolt user-engine host, for example account-1-mindcloud.api.us-east-1.app.firebolt.io. |
| `engineName` | query | `string` | no | Optional user engine name when routing through a shared user-engine host. |
| `database` | query | `string` | no | Optional database to target for the merge statement. |
| `targetTableName` | body | `string` | yes | Target table to merge into. |
| `sourceClause` | body | `string` | yes | USING clause source, such as a SELECT subquery with an alias. |
| `joinCondition` | body | `string` | yes | ON clause that matches source rows to target rows. |
| `whenClauses` | body | `string` | yes | One or more WHEN clauses that define the merge behavior. |
