# Download Processed File with Verify550

Downloads a processed file from Verify550.

## Endpoint

- **Method:** `GET`
- **Path:** `/file`
- **Base URL:** `https://app.verify550.com/api`
- **Official documentation:** [Download Processed File](https://verify550.com/documentation/endpoint-specifications/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | Verify550 file identifier. |
| `type` | query | `string` | yes | Which processed result file to download. Accepted values: `clean`, `full`. |
