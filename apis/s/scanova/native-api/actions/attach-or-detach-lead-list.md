# Attach Or Detach Lead List with Scanova

## Endpoint

- **Method:** `PATCH`
- **Path:** `/qr/{qrid}/`
- **Base URL:** `https://management.scanova.io`
- **Official documentation:** [Attach Or Detach Lead List](https://docs.scanova.io/api-reference/endpoint/lead_list/attach)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `qrid` | path | `string` | yes | QR code ID |
| `lead_list` | body | `string` | yes | Set to null to detach lead list from QR code |
