# Resend Verify Code SMS With Lookup with Mocean API

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/2/verify/resend/sms?mocean-resp-format=json&mocean-request-nl=1`
- **Base URL:** `https://rest.moceanapi.com`
- **Official documentation:** [Resend Verify Code SMS With Lookup](https://moceanapi.com/docs#resend-code-over-sms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mocean-reqid` | query | `string` | yes | Verify request ID returned by Mocean. |
