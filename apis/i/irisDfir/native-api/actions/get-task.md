# Get Task with Iris Dfir

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/cases/:case_identifier/tasks/:identifier`
- **Base URL:** `https://v200.beta.dfir-iris.org`
- **Official documentation:** [Get Task](https://docs.dfir-iris.org/latest/_static/iris_api_reference_v2.1.0.html#tag/Tasks/operation/api_v2_cases_(case_identifier)_tasks_(identifier)_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `case_identifier` | path | `number` | yes | IRIS case identifier. |
| `identifier` | path | `number` | yes | IRIS task identifier. |
