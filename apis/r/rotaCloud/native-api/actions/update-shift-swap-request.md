# Update Shift Swap Request with RotaCloud

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/swap_requests/:id`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Update Shift Swap Request](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `admin_approved` | body | `boolean` | yes | Whether the admin approved the swap request. |
| `id` | path | `number` | yes | Shift swap request ID. |
