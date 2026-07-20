# Get Lean Scan with Cursion

Retrieves abbreviated scan details from Cursion.

## Endpoint

- **Method:** `GET`
- **Path:** `/scan/{{scanId}}/lean`
- **Base URL:** `https://api.cursion.dev/v1/ops`
- **Official documentation:** [Get Lean Scan](https://docs.cursion.dev/api/scan)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scanId` | path | `string` | yes | The scan identifier. |
