# Get SIP Status with Novofon

Retrieves SIP status from Novofon.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/sip/:sipId/status/`
- **Base URL:** `https://api.novofon.com`
- **Official documentation:** [Get SIP Status](https://novofon.com/instructions/api/#sip_status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sipId` | path | `string` | yes | SIP account identifier to check. |
