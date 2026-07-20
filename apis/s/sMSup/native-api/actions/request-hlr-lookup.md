# Request HLR Lookup with SMSup

## Endpoint

- **Method:** `POST`
- **Path:** `/api/hlr/request`
- **Base URL:** `https://api.gateway360.com`
- **Official documentation:** [Request HLR Lookup](https://app.smsup.es/api/3.0/docs/hlr/lookup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `msisdn` | body | `string` | yes | Mobile number in international format. |
