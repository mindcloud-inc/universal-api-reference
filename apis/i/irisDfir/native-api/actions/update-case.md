# Update Case with Iris Dfir

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/cases/:case_identifier`
- **Base URL:** `https://v200.beta.dfir-iris.org`
- **Official documentation:** [Update Case](https://docs.dfir-iris.org/latest/_static/iris_api_reference_v2.1.0.html#tag/Cases/operation/api_v2_cases_(case_identifier)_put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `case_identifier` | path | `number` | yes | IRIS case identifier. |
| `case_name` | body | `string` | yes | Updated case name. |
| `case_description` | body | `string` | yes | Updated case description. |
| `case_customer` | body | `number` | yes | Customer id for the updated case. |
| `case_soc_id` | body | `string` | yes | Updated SOC ticket reference. |
