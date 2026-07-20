# Expand Short Link with TLY Link Shortener

Expands a short link in TLY Link Shortener.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/link/expand`
- **Base URL:** `https://api.t.ly`
- **Official documentation:** [Expand Short Link](https://t.ly/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `short_url` | body | `string` | yes | The short URL to expand. |
| `password` | body | `string` | no | Password for protected short links. |
