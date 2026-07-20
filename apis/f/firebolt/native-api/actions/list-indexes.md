# List Indexes with Firebolt

Retrieves indexes from Firebolt.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineUrl`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [List Indexes](https://docs.firebolt.io/reference-sql/commands/metadata/show-indexes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineUrl` | path | `string` | yes | Firebolt user engine host, for example account-1-mindcloud.api.us-east-1.app.firebolt.io. |
| `engineName` | query | `string` | yes | Name of the user engine, for example mc_fb_act_20260422_engine. |
| `database` | query | `string` | yes | Database to use for the statement. |
