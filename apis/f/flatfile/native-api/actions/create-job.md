# Create Job with Flatfile

Creates a new job in Flatfile.

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs`
- **Base URL:** `https://api.x.flatfile.com/v1`
- **Official documentation:** [Create Job](https://reference.flatfile.com/api-reference/jobs/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `operation` | body | `string` | yes | Job operation. |
| `source` | body | `string` | yes | Job source descriptor. |
| `type` | body | `string` | yes | Job type. |
