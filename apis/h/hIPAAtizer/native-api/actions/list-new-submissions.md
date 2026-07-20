# List New Submissions with HIPAAtizer

Retrieves new submissions from HIPAAtizer by workflow or location.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/api_key/submissions/unconfirmed_list`
- **Base URL:** `https://app.hipaatizer.com`
- **Official documentation:** [List New Submissions](https://github.com/HIPAAtizer/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request` | body | `object` | no | Optional raw request wrapper. Use `{}` when running without filters. |
| `request.locationIds` | body | `list<string>` | no | Optional location UUID filters. |
| `request.workflowIds` | body | `list<string>` | no | Optional workflow UUID filters. |
