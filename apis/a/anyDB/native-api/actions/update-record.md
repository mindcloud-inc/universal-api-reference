# Update Record with AnyDB

Updates an existing record in AnyDB.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/integrations/ext/updaterecord`
- **Base URL:** `https://app.anydb.com`
- **Official documentation:** [Update Record](https://www.anydb.com/openapi/spec.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meta` | body | `object` | yes | The AnyDB meta object describing the record update, including adoid, adbid, teamid, and icon. |
| `content[]` | body | `array<object>` | no | Optional AnyDB content array payload for the update. |
