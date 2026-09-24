# List Worker Leaves with ADP

## Endpoint

- **Method:** `GET`
- **Path:** `hr/v2/workers/:aoid/leaves`
- **Base URL:** `https://api.adp.com/`
- **Official documentation:** [List Worker Leaves](https://developers.adp.com/apis/api-explorer/hcm-offrg-wfn/hcm-offrg-wfn-hr-worker-leaves-v2-worker-leaves?operation=GET%2Fhr%2Fv2%2Fworkers%2F%7Baoid%7D%2Fleaves#swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `aoid` | path | `string` | yes | The ADP associate object identifier for the worker whose leave records should be returned. |
