# ZUGFeRD To JSON with finaX

Retrieves invoice JSON from a ZUGFeRD file in finaX.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/json/zugferd/`
- **Base URL:** `https://api.finax.dev`
- **Official documentation:** [ZUGFeRD To JSON](https://docs.finax.dev/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | ZUGFeRD invoice file. |
