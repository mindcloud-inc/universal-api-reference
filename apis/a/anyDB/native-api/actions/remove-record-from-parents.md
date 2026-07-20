# Remove Record From Parents with AnyDB

Removes a record from parent records in AnyDB.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/integrations/ext/remove`
- **Base URL:** `https://app.anydb.com`
- **Official documentation:** [Remove Record From Parents](https://www.anydb.com/openapi/spec.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adoid` | body | `string` | yes | The AnyDB record ID. |
| `adbid` | body | `string` | yes | The AnyDB database ID. |
| `teamid` | body | `string` | yes | The AnyDB team ID. |
| `removefromids` | body | `string<string>` | yes | Comma-separated AnyDB parent IDs to detach the record from. |
