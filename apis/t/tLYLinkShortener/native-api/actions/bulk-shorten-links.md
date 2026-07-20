# Bulk Shorten Links with TLY Link Shortener

Creates short links in bulk in TLY Link Shortener.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/link/bulk`
- **Base URL:** `https://api.t.ly`
- **Official documentation:** [Bulk Shorten Links](https://t.ly/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `links[]` | body | `array<string>` | yes | List of destination URLs to shorten in bulk. |
| `domain` | body | `string` | no | Optional branded domain to use for every generated short link. |
| `tags[]` | body | `array<number>` | no | Optional tag IDs to attach to every generated short link. |
| `pixels[]` | body | `array<number>` | no | Optional pixel IDs to attach to every generated short link. |
