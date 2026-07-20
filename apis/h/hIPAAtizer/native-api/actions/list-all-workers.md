# List All Workers with HIPAAtizer

Retrieves workers from HIPAAtizer for selected locations.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/api_key/workers/all`
- **Base URL:** `https://app.hipaatizer.com`
- **Official documentation:** [List All Workers](https://github.com/HIPAAtizer/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request` | body | `object` | no | Optional raw request wrapper. Use `{}` when running without filters. |
| `request.locationIds` | body | `list<string>` | no | Optional location UUID filters. |
