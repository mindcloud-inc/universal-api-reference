# Request PIN with SMSup

## Endpoint

- **Method:** `POST`
- **Path:** `/api/2fa/request`
- **Base URL:** `https://api.gateway360.com`
- **Official documentation:** [Request PIN](https://app.smsup.es/api/3.0/docs/2factor/request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `msisdn` | body | `string` | yes | Mobile number to verify in international format. |
| `sender` | body | `string` | no | Sender field for the SMS. |
| `hlr_lookup` | body | `number` | no | Set to 1 to require a successful HLR lookup before sending. |
