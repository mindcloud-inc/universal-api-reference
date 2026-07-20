# Update Alert Triage with Socket

Creates or updates alert triage rules in Socket.

## Endpoint

- **Method:** `POST`
- **Path:** `/orgs/:org_slug/triage/alerts`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [Update Alert Triage](https://docs.socket.dev/reference/updateorgalerttriage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alertKey` | body | `string` | no | — |
| `alertTriage[]` | body | `array<object>` | no | — |
| `note` | body | `string` | no | — |
| `state` | body | `string` | no | One of block, ignore, inherit, monitor, or warn. |
