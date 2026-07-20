# Update Estimate Status with RO App

## Endpoint

- **Method:** `POST`
- **Path:** `/estimates/:estimate_id/status`
- **Base URL:** `https://api.roapp.io/v2`
- **Official documentation:** [Update Estimate Status](https://roapp.readme.io/reference/change-estimate-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `estimate_id` | path | `number` | yes | Estimate ID |
| `status_id` | body | `number` | yes | Status Id |
| `comment` | body | `string` | no | Status comment |
