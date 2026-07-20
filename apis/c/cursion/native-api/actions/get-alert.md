# Get Alert with Cursion

Retrieves an existing alert from Cursion.

## Endpoint

- **Method:** `GET`
- **Path:** `/alert/{{alertId}}`
- **Base URL:** `https://api.cursion.dev/v1/ops`
- **Official documentation:** [Get Alert](https://docs.cursion.dev/api/alert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alertId` | path | `string` | yes | The alert identifier. |
