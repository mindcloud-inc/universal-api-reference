# Retrieve Job Results with DocuProx

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/job-results`
- **Base URL:** `https://api.docuprox.com`
- **Official documentation:** [Retrieve Job Results](https://docuprox.com/docs/api/#job-results-endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | body | `string` | yes | UUID of the completed job to fetch results for. |
| `result_format` | body | `string` | no | Output format: json or csv. |
