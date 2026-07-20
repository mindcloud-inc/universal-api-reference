# Check Blacklists with EmailListVerify

Checks IP or domain blacklists in EmailListVerify.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/checkBlacklists`
- **Base URL:** `https://api.emaillistverify.com`
- **Official documentation:** [Check Blacklists](https://api.emaillistverify.com/api-doc#/Verification%20Endpoints/checkBlacklists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `value` | body | `string` | yes | IP address or domain to check against DNS-based blacklists. |
