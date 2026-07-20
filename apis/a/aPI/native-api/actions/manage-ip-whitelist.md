# Manage IP Whitelist with 44API

Manages the IP whitelist in 44API by adding, removing, or listing IPs.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhook/ip-whitelist`
- **Base URL:** `https://api.44api.dev`
- **Official documentation:** [Manage IP Whitelist](https://docs.44api.dev)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | body | `string` | yes | Use add, remove, or list. |
| `ipAddress` | body | `string` | no | IP address required for add and remove actions. |
| `email` | body | `string` | no | Verification email required for add. |
