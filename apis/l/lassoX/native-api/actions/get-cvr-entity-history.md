# Get CVR Entity History with Lasso X

Retrieves CVR entity history from Lasso X by Lasso ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/:lassoId/history`
- **Base URL:** `https://api.lassox.com`
- **Official documentation:** [Get CVR Entity History](https://docs.lassox.com/data-apis/cvr/#basic-info-staminformation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lassoId` | path | `string` | yes | Lasso ID, for example CVR-1-34580820. |
