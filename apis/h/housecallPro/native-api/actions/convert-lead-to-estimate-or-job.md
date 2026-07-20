# Convert Lead to Estimate or Job with Housecall Pro

## Endpoint

- **Method:** `POST`
- **Path:** `/leads/:id/convert`
- **Base URL:** `https://api.housecallpro.com`
- **Official documentation:** [Convert Lead to Estimate or Job](https://docs.housecallpro.com/docs/housecall-public-api/d9c8a89ed4e4c-convert-lead-to-estimate-or-job)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the lead to convert. |
| `type` | body | `list` | yes | Must be either estimate or job. Accepted values: `estimate`, `job`. |
