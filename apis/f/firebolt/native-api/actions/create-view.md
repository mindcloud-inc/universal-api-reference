# Create View with Firebolt

Creates a new view in Firebolt.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineUrl`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Create View](https://docs.firebolt.io/reference-sql/commands/data-definition/create-view)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineUrl` | path | `string` | yes | Firebolt user engine host, for example account-1-mindcloud.api.us-east-1.app.firebolt.io. |
| `engineName` | query | `string` | yes | Name of the user engine, for example mc_fb_act_20260422_engine. |
| `database` | query | `string` | yes | Database to use for the statement. |
| `viewName` | body | `string` | yes | Name of the view to create. |
| `selectStatement` | body | `string` | yes | SELECT statement that defines the view. |
