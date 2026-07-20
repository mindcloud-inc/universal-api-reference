# Check Verify Code with Mocean API

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/2/verify/check?mocean-resp-format=json`
- **Base URL:** `https://rest.moceanapi.com`
- **Official documentation:** [Check Verify Code](https://moceanapi.com/docs#verify-code)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mocean-code` | query | `string` | yes | Verification code to check. |
| `mocean-reqid` | query | `string` | yes | Verify request ID returned by Mocean. |
