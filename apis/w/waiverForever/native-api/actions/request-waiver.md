# Request Waiver with WaiverForever

Creates a waiver request link from a WaiverForever template.

## Endpoint

- **Method:** `GET`
- **Path:** `/openapi/v1/template/:template_id/requestWaiver`
- **Base URL:** `https://api.waiverforever.com`
- **Official documentation:** [Request Waiver](https://docs.waiverforever.com/#request-waiver)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | path | `string` | yes | WaiverForever template identifier. |
| `ttl` | query | `number` | no | Requested waiver expiration time in seconds. Defaults to 86400 when omitted. |
