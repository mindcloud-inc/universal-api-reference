# Create Source with BigML

Creates a source in BigML.

## Endpoint

- **Method:** `POST`
- **Path:** `/source`
- **Base URL:** `https://bigml.io`
- **Official documentation:** [Create Source](https://bigml.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `remote` | body | `string` | yes | Publicly reachable URL for the source data file (CSV, TSV, JSON, ZIP, etc.). |
