# Get Tour with Storyscale

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/tour/view/{tour_id}/`
- **Base URL:** `https://prodapi.storyscale.com/api`
- **Official documentation:** [Get Tour](https://prodapi.storyscale.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tour_id` | path | `string` | yes | The Storyscale tour ID. |
| `with_screens` | query | `boolean` | no | Include tour screens in the response. |
