# Get QR Code List with Scanova

## Endpoint

- **Method:** `GET`
- **Path:** `/qr/`
- **Base URL:** `https://management.scanova.io`
- **Official documentation:** [Get QR Code List](https://docs.scanova.io/api-reference/endpoint/qr_manager/get)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_from` | query | `date` | no | Filter QR codes created from this date (YYYY-MM-DD) |
| `created_till` | query | `date` | no | Filter QR codes created till this date (YYYY-MM-DD) |
| `qrid` | query | `string` | no | Filter by specific QR code ID(s). Must be a comma-separated list of QR IDs. Example: Q349...,Qf94... Send multiple values as a string separated by `,`. |
| `tags` | query | `string` | no | Filter by tags (comma-separated, URL encoded) Send multiple values as a string separated by `,`. |
| `category` | query | `string` | no | Filter by category slugs (comma-separated, URL encoded) Send multiple values as a string separated by `,`. |
| `type` | query | `string` | no | Filter by QR code type |
| `status` | query | `string` | no | Filter by QR code status |
| `users` | query | `string` | no | Filter by user IDs (comma-separated, URL encoded) Send multiple values as a string separated by `,`. |
| `scan_type` | query | `string` | no | Filter by scan count comparison type |
| `scan_count1` | query | `number` | no | Primary scan count value (required with scan_type) |
| `scan_count2` | query | `number` | no | Secondary scan count value (required for 'between' scan_type) |
| `search` | query | `string` | no | Search value |
| `search_fields` | query | `string` | no | Fields to search in (comma-separated) Send multiple values as a string separated by `,`. |
