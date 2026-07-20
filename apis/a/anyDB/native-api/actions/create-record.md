# Create Record with AnyDB

Creates a new record in AnyDB.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/integrations/ext/createrecord`
- **Base URL:** `https://app.anydb.com`
- **Official documentation:** [Create Record](https://www.anydb.com/openapi/spec.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adbid` | body | `string` | yes | The AnyDB database ID. |
| `teamid` | body | `string` | yes | The AnyDB team ID. |
| `name` | body | `string` | yes | The AnyDB record name. |
| `attach` | body | `string` | no | Optional AnyDB parent ID to attach the created record to. |
| `template` | body | `string` | no | Optional AnyDB template ID for the created record. |
| `templatename` | body | `string` | no | Optional AnyDB template name for the created record. |
| `content[]` | body | `array<object>` | no | Optional AnyDB content array for the created record. |
