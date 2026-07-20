# Request Call Recording with Novofon

Retrieves call recording links from Novofon.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/pbx/record/request/`
- **Base URL:** `https://api.novofon.com`
- **Official documentation:** [Request Call Recording](https://novofon.com/instructions/api/#record)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `call_id` | query | `string` | no | Unique call ID from the statistics response. |
| `lifetime` | query | `string` | no | Optional link lifetime in seconds. Docs say minimum 180, maximum 5184000, default 1800. |
| `pbx_call_id` | query | `string` | no | Persistent PBX call ID that can return multiple recording links. |
