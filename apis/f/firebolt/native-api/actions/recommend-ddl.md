# Recommend DDL with Firebolt

Retrieves DDL recommendations from Firebolt.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineUrl`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Recommend DDL](https://docs.firebolt.io/reference-sql/commands/queries/recommend_ddl)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineUrl` | path | `string` | yes | Firebolt user engine host, for example account-1-mindcloud.api.us-east-1.app.firebolt.io. |
| `engineName` | query | `string` | yes | Name of the user engine, for example mc_fb_act_20260422_engine. |
| `database` | query | `string` | yes | Database to use for the statement. |
| `tableName` | body | `string` | yes | Table name to optimize. |
| `workloadQuery` | body | `string` | yes | SELECT statement that returns exactly one TEXT column containing workload SQL. |
