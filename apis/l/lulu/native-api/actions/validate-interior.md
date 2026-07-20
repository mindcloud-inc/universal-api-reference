# Validate Interior with Lulu

Validates an interior file in Lulu.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate-interior/`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Validate Interior](https://api.lulu.com/docs/#tag/Validate-Interior/operation/Validate-Interior_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_url` | body | `string` | yes | Publicly reachable Lulu interior file URL. |
| `pod_package_id` | body | `string` | no | Lulu pod package ID used for interior validation. |
