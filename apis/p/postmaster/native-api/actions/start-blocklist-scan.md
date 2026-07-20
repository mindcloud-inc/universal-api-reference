# Start Blocklist Scan with Postmaster+

Starts a blocklist scan in Postmaster+.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/blocklist/scan/start`
- **Base URL:** `https://postmasterplus.app`
- **Official documentation:** [Start Blocklist Scan](https://postmasterplus.app/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `follow_redirects` | body | `boolean` | no | Whether to follow redirects and scan all hosts in the redirect chain. |
| `urls` | body | `list<string>` | yes | Array of URLs to scan, between 1 and 100 URLs. |
