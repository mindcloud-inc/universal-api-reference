# Copy To S3 with Firebolt

Creates a copy-to-S3 operation in Firebolt.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineHost`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Copy To S3](https://docs.firebolt.io/reference-sql/commands/data-management/copy-to)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineHost` | path | `string` | yes | Firebolt user-engine host, for example account-1-mindcloud.api.us-east-1.app.firebolt.io. |
| `engineName` | query | `string` | no | Optional user engine name when routing through a shared user-engine host. |
| `database` | query | `string` | no | Optional database to target for the COPY TO statement. |
| `selectQuery` | body | `string` | yes | SELECT query whose results should be exported. |
| `destination` | body | `string` | yes | An Amazon S3 URL or Firebolt location object name to copy data to. |
| `copyOptions` | body | `string` | no | Optional COPY TO options. For URL destinations that need access configuration, include the CREDENTIALS = (...) clause here. |
