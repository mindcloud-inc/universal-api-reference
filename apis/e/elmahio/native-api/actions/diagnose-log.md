# Diagnose Log with elmah.io

Retrieves log diagnostics from elmah.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/logs/:id/_diagnose`
- **Base URL:** `https://api.elmah.io`
- **Official documentation:** [Diagnose Log](https://api.elmah.io/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the log to diagnose. |
