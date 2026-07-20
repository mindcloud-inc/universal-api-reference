# Verify 2FA PIN with Infobip

## Endpoint

- **Method:** `POST`
- **Path:** `/2fa/2/pin/{pinId}/verify`
- **Base URL:** `https://rkpzwe.api.infobip.com`
- **Official documentation:** [Verify 2FA PIN](https://www.infobip.com/docs/api/platform/2fa/pin-sending-and-verification/verify-2fa-phone-number)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pinId` | path | `string` | yes | ID of the pin code that has to be verified. |
| `pin` | body | `string` | yes | The PIN code to verify. |
