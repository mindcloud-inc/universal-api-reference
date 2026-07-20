# Check Async Query Status with Firebolt

Retrieves asynchronous query status from Firebolt.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineUrl`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Check Async Query Status](https://docs.firebolt.io/reference-api/using-async-queries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineUrl` | path | `string` | yes | Firebolt engine URL host or engine endpoint used to check async query status. |
| `database` | query | `string` | no | Database to target for user-engine async status checks when required. |
| `engineName` | query | `string` | no | User engine name to target when checking async query status on a user engine. |
| `asyncToken` | body | `string` | yes | Async query token returned by Firebolt. |
