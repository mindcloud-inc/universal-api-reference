# Validate Cover with Lulu

Validates a cover file in Lulu.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate-cover/`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Validate Cover](https://api.lulu.com/docs/#tag/Validate-Cover/operation/Validate-Cover_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_url` | body | `string` | yes | Publicly reachable Lulu cover file URL. |
| `pod_package_id` | body | `string` | yes | Lulu pod package ID used for cover validation. |
| `interior_page_count` | body | `number` | yes | Interior page count for the cover validation request. |
