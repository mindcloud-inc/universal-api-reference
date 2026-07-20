# Copy From S3 with Firebolt

Creates a copy-from-S3 operation in Firebolt.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineHost`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Copy From S3](https://docs.firebolt.io/reference-sql/commands/data-management/copy-from)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineHost` | path | `string` | yes | Firebolt user-engine host, for example account-1-mindcloud.api.us-east-1.app.firebolt.io. |
| `engineName` | query | `string` | no | Optional user engine name when routing through a shared user-engine host. |
| `database` | query | `string` | no | Optional database to target for the COPY FROM statement. |
| `tableName` | body | `string` | yes | Target table to copy data into. |
| `source` | body | `string` | yes | An Amazon S3 URL or Firebolt location object name to copy data from. |
| `copyOptions` | body | `string` | no | Optional COPY FROM options. For URL sources that need access configuration, include the CREDENTIALS = (...) clause here. |
