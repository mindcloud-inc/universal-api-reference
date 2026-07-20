# Bulk Update Links with TLY Link Shortener

Updates short links in bulk in TLY Link Shortener.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/link/bulk/update`
- **Base URL:** `https://api.t.ly`
- **Official documentation:** [Bulk Update Links](https://t.ly/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `links[]` | body | `array<string>` | yes | List of short URLs to update in bulk. |
| `tags[]` | body | `array<number>` | no | Optional replacement tag IDs for the provided links. |
| `pixels[]` | body | `array<number>` | no | Optional replacement pixel IDs for the provided links. |
