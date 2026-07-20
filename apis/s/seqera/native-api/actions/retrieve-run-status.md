# Retrieve Run Status with Seqera

Retrieves a workflow run status from Seqera.

## Endpoint

- **Method:** `GET`
- **Path:** `/ga4gh/wes/v1/runs/:run_id/status`
- **Base URL:** `https://api.cloud.seqera.io`
- **Official documentation:** [Retrieve Run Status](https://cloud.seqera.io/openapi/seqera-api-latest.yml)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `run_id` | path | `string` | yes |
