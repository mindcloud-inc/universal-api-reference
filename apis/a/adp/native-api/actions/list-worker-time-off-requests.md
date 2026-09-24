# List Worker Time Off Requests with ADP

## Endpoint

- **Method:** `GET`
- **Path:** `time/v2/workers/:aoid/time-off-details/time-off-requests`
- **Base URL:** `https://api.adp.com/`
- **Official documentation:** [List Worker Time Off Requests](https://developers.adp.com/apis/api-explorer/hcm-offrg-wfn/hcm-offrg-wfn-time-time-off-requests-v2-time-off-requests?operation=GET%2Ftime%2Fv2%2Fworkers%2F%7Baoid%7D%2Ftime-off-details%2Ftime-off-requests#swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `aoid` | path | `string` | yes | The ADP associate object identifier for the worker whose time-off requests should be returned. |
