# Create Job Note with ServiceTitan

## Endpoint

- **Method:** `POST`
- **Path:** `jpm/v2/tenant/{tenant}/jobs/:id/notes`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Create Job Note](https://developer.servicetitan.io/api-details/#api=tenant-jpm-v2&operation=Projects_CreateNote)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | no |
| `text` | body | `string` | no |
| `pinToTop` | body | `boolean` | no |
