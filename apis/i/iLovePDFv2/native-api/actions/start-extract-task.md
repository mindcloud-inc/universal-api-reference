# Start Extract PDF Task with iLovePDFv2

Starts a PDF extraction task in iLovePDFv2.

## Endpoint

- **Method:** `GET`
- **Path:** `/start/extract/:region`
- **Base URL:** `https://api.ilovepdf.com/v1`
- **Official documentation:** [Start Extract PDF Task](https://www.iloveapi.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `region` | path | `list` | yes | Processing region / jurisdiction. Accepted values: `0`, `1`, `2`, `3`, `4`. |
