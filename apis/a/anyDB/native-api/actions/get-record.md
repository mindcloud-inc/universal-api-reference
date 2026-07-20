# Get Record with AnyDB

Retrieves a record from AnyDB by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/integrations/ext/record`
- **Base URL:** `https://app.anydb.com`
- **Official documentation:** [Get Record](https://www.anydb.com/openapi/spec.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamid` | query | `string` | yes | The AnyDB team ID. |
| `adbid` | query | `string` | yes | The AnyDB database ID. |
| `adoid` | query | `string` | yes | The AnyDB record ID. |
