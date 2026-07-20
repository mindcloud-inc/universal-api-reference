# CII Invoice Xml with finaX

Creates CII invoice XML from JSON in finaX.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/xml/cii/`
- **Base URL:** `https://api.finax.dev`
- **Official documentation:** [CII Invoice Xml](https://docs.finax.dev/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice` | body | `object` | yes | Invoice payload to convert to CII XML. |
