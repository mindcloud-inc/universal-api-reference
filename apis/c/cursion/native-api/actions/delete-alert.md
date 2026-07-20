# Delete Alert with Cursion

Deletes an existing alert from Cursion.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/alert/{{alertId}}`
- **Base URL:** `https://api.cursion.dev/v1/ops`
- **Official documentation:** [Delete Alert](https://docs.cursion.dev/api/alert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alertId` | path | `string` | yes | The alert identifier. |
