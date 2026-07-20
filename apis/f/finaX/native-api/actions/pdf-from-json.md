# PDF From JSON with finaX

Creates a ZUGFeRD PDF from invoice JSON in finaX.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/pdf/json/`
- **Base URL:** `https://api.finax.dev`
- **Official documentation:** [PDF From JSON](https://docs.finax.dev/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice` | body | `object` | yes | Invoice payload. |
| `config` | body | `object` | yes | Render configuration. |
