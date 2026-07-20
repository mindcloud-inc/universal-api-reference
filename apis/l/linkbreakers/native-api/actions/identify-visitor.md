# Identify Visitor with Linkbreakers

Identifies a visitor record within Linkbreakers.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/visitor/identify`
- **Base URL:** `https://api.linkbreakers.com`
- **Official documentation:** [Identify Visitor](https://linkbreakers.com/help/api/visitors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lbid` | body | `string` | no | LBID that initiated the visit. |
| `setOnce` | body | `boolean` | no | Only set fields that are currently empty. |
| `visitor` | body | `object` | no | Visitor identification payload. |
