# UBL Invoice Xml with finaX

Creates UBL invoice XML from JSON in finaX.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/xml/ubl/`
- **Base URL:** `https://api.finax.dev`
- **Official documentation:** [UBL Invoice Xml](https://docs.finax.dev/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice` | body | `object` | yes | Invoice payload to convert to UBL XML. |
