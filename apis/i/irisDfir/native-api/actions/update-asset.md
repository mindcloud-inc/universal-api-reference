# Update Asset with Iris Dfir

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/cases/:case_identifier/assets/:identifier`
- **Base URL:** `https://v200.beta.dfir-iris.org`
- **Official documentation:** [Update Asset](https://docs.dfir-iris.org/latest/_static/iris_api_reference_v2.1.0.html#tag/Assets/operation/api_v2_cases_(case_identifier)_assets_(identifier)_put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asset_name` | body | `string` | yes | Name of the asset. |
| `asset_type_id` | body | `number` | yes | IRIS asset type identifier. |
| `case_identifier` | path | `number` | yes | IRIS case identifier. |
| `identifier` | path | `number` | yes | IRIS asset identifier. |
