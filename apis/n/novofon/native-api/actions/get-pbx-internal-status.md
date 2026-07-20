# Get PBX Internal Status with Novofon

Retrieves PBX internal status from Novofon.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/pbx/internal/:pbxSip/status/`
- **Base URL:** `https://api.novofon.com`
- **Official documentation:** [Get PBX Internal Status](https://novofon.com/instructions/api/#pbx_internal_status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pbxSip` | path | `string` | yes | PBX internal number to check. |
