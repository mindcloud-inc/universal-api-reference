# Get Download URL with AnyDB

Retrieves a download URL for an AnyDB attachment.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/integrations/ext/download`
- **Base URL:** `https://app.anydb.com`
- **Official documentation:** [Get Download URL](https://www.anydb.com/openapi/spec.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamid` | query | `string` | yes | The AnyDB team ID. |
| `adbid` | query | `string` | yes | The AnyDB database ID. |
| `adoid` | query | `string` | yes | The AnyDB record ID. |
| `cellpos` | query | `string` | yes | The cell position to download. |
| `redirect` | query | `boolean` | no | Whether AnyDB should return an HTTP redirect instead of a JSON payload. |
| `preview` | query | `boolean` | no | Whether AnyDB should generate a preview download. |
