# Get Company (v2) with gBizINFO

Retrieves company details from gBizINFO by corporate number.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/hojin/:corporate_number`
- **Base URL:** `https://api.info.gbiz.go.jp/hojin`
- **Official documentation:** [Get Company (v2)](https://api.info.gbiz.go.jp/hojin/swagger-ui/index.html#/gBizINFO_REST_API/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `corporate_number` | path | `string` | yes | The 13-digit Japanese corporate number to look up. |
| `metadata_flg` | query | `boolean` | no | Include metadata fields in the company response. |
