# Update Sandbox Network with E2B

Updates sandbox network settings in E2B.

## Endpoint

- **Method:** `PUT`
- **Path:** `/sandboxes/{sandboxID}/network`
- **Base URL:** `https://api.e2b.app`
- **Official documentation:** [Update Sandbox Network](https://e2b.dev/docs/api-reference/sandboxes/put-sandboxes-network)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `allowOut[]` | body | `array<string>` | no | Allowed CIDR blocks, IP addresses, or domain names for sandbox egress traffic. |
| `denyOut[]` | body | `array<string>` | no | Denied CIDR blocks or IP addresses for sandbox egress traffic. |
| `sandboxID` | path | `string` | yes | Identifier of the sandbox. |
