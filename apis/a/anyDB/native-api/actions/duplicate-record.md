# Duplicate Record with AnyDB

Creates a duplicate record in AnyDB.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/integrations/ext/copyrecord`
- **Base URL:** `https://app.anydb.com`
- **Official documentation:** [Duplicate Record](https://www.anydb.com/openapi/spec.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adoid` | body | `string` | yes | The AnyDB record ID to duplicate. |
| `adbid` | body | `string` | yes | The AnyDB database ID containing the record. |
| `teamid` | body | `string` | yes | The AnyDB team ID containing the record. |
| `dstadbid` | body | `string` | no | Optional destination database ID for the duplicate. |
| `attachto` | body | `string` | no | Optional parent ID to attach the duplicate to. |
| `attachmentsmode` | body | `string` | no | Optional attachment handling mode: noattachments, link, or duplicate. |
