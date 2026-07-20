# Create Case with Iris Dfir

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/cases`
- **Base URL:** `https://v200.beta.dfir-iris.org`
- **Official documentation:** [Create Case](https://docs.dfir-iris.org/latest/_static/iris_api_reference_v2.1.0.html#tag/Cases/operation/api_v2_cases_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `case_customer` | body | `number` | yes | Customer linked to the case. |
| `case_description` | body | `string` | yes | Short summary of the case. |
| `case_name` | body | `string` | yes | Short name for the case. |
| `case_soc_id` | body | `string` | yes | SOC ticket reference for the case. |
