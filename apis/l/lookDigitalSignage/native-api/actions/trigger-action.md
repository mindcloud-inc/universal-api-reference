# Trigger Action with Look Digital Signage

Triggers a configured action in Look Digital Signage.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.lookit.hk/api/v1/external/actions/:actionLink`
- **Base URL:** `https://api.lookit.hk/api/v1/external/actions`
- **Official documentation:** [Trigger Action](https://www.lookdigitalsignage.com/knowledge-base/create-action-trigger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actionLink` | path | `string` | yes | Paste the full Action Link from Look Action settings. |
