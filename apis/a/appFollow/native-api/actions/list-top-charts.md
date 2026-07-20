# List Top Charts with AppFollow

Retrieves top chart results from AppFollow.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/charts/topcharts`
- **Base URL:** `https://api.appfollow.io`
- **Official documentation:** [List Top Charts](https://docs.api.appfollow.io/reference/public_top_charts_api_v2_charts_topcharts_get-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | yes | Country code. |
| `device` | query | `string` | yes | Device type. |
| `genre` | query | `string` | yes | Genre code. |
| `date` | query | `string` | yes | Date. |
