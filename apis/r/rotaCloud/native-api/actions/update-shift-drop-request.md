# Update Shift Drop Request with RotaCloud

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/unavailability_requests/:id/:decision`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Update Shift Drop Request](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `decision` | path | `string` | yes | Decision path segment, such as approve or deny. |
| `id` | path | `number` | yes | Shift drop request ID. |
| `message` | body | `string` | yes | Reply message for the shift drop request. |
