# Create Batch Request with Proofy

## Endpoint

- **Method:** `POST`
- **Path:** `/verify/batch/create`
- **Base URL:** `https://apis.proofy.io/v1`
- **Official documentation:** [Create Batch Request](https://docs.proofy.io/api-reference/endpoint/verify-batch-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | yes | Email addresses to verify in one batch request. |
