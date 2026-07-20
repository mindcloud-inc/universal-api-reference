# Resend Verify Code SMS with Mocean API

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/2/verify/resend/sms?mocean-resp-format=json`
- **Base URL:** `https://rest.moceanapi.com`
- **Official documentation:** [Resend Verify Code SMS](https://moceanapi.com/docs#resend-code-over-sms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mocean-reqid` | query | `string` | yes | Verify request ID returned by Mocean. |
