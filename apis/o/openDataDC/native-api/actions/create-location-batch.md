# Create Location Batch with Open Data DC

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2.2/locationbatch`
- **Base URL:** `https://datagate.dc.gov/mar/open`
- **Official documentation:** [Create Location Batch](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address_base64` | body | `string` | yes | Base64 encoded addresses in JSON object. |
