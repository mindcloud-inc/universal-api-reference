# Cancel Query with Firebolt

Deletes a running query from Firebolt.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineUrl`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Cancel Query](https://docs.firebolt.io/reference-sql/commands/queries/cancel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineUrl` | path | `string` | yes | Firebolt engine URL host used to cancel the query. |
| `engineName` | query | `string` | no | User engine name used to run the cancel command. |
| `database` | query | `string` | no | Database to target for user-engine cancel commands when required. |
| `queryId` | body | `string` | yes | Firebolt query id to cancel. |
