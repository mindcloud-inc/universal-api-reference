# Send Verify Code SMS With Lookup with Mocean API

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/2/verify/req/sms?mocean-resp-format=json&mocean-request-nl=1`
- **Base URL:** `https://rest.moceanapi.com`
- **Official documentation:** [Send Verify Code SMS With Lookup](https://moceanapi.com/docs#send-code-over-sms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mocean-brand` | query | `string` | yes | Brand or application name for the verification message. |
| `mocean-from` | query | `string` | no | Optional sender ID for the verification SMS. |
| `mocean-to` | query | `string` | yes | Recipient phone number with country code. |
