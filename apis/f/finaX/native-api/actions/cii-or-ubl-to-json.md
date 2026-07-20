# CII Or UBL To JSON with finaX

Retrieves invoice JSON from CII or UBL XML in finaX.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/json/xml/`
- **Base URL:** `https://api.finax.dev`
- **Official documentation:** [CII Or UBL To JSON](https://docs.finax.dev/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Invoice XML file. |
