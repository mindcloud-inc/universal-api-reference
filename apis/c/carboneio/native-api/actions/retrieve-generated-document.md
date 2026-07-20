# Retrieve Generated Document with Carbone.io

Downloads a generated document from Carbone.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/render/:renderId`
- **Base URL:** `https://api.carbone.io`
- **Official documentation:** [Retrieve Generated Document](https://carbone.io/documentation/developer/http-api/download-reports.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `renderId` | path | `string` | yes | Render ID returned by a previous generate or convert request. |
