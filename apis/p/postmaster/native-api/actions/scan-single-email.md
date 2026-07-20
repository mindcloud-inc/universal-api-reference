# Scan Single Email with Postmaster+

Scans a single email in Postmaster+.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/intelligence/single-emails/scan`
- **Base URL:** `https://postmasterplus.app`
- **Official documentation:** [Scan Single Email](https://postmasterplus.app/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actions` | body | `string` | no | Comma-separated intelligence actions to run. |
| `email` | body | `string` | yes | The email address to scan. |
