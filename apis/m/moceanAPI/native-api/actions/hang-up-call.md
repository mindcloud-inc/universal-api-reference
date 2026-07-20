# Hang Up Call with Mocean API

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/2/voice/hangup?mocean-resp-format=json`
- **Base URL:** `https://rest.moceanapi.com`
- **Official documentation:** [Hang Up Call](https://moceanapi.com/docs#hangup-a-call)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mocean-call-uuid` | query | `string` | yes | The call UUID to hang up. |
